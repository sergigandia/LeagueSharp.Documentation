# Load.OnLoad
OnLoad is and event where your l# code start to works and it happens when your l# is injected and the game is started.

# How to call Load.OnLoad event?

you need to create the funciton OnLoad like this : 
```c#
 public void yourname(EventArgs args)
        {
        //here go the code to start 
        //load menu
        //update
        // draws
        }
```
*yourname is the name you put to your load method.
      
Then we need to add in your main method or where you wanna call the load the next lane :
```c#
      CustomEvents.Game.OnGameLoad += p.load;
```c#
And it will work
example we are going to create hello world in the load event: 
```c#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using LeagueSharp;
using LeagueSharp.Common;
using SharpDX;
using System.Drawing;
namespace YourAssemblyName
{
    class Program 
    {
            static void Main(string[] args)
        {
           CustomEvents.Game.OnGameLoad += load;
        }
        public void load(EventArgs args)
        {
             Notifications.AddNotification(new Notification("HELLO WORLD!", duration, dispose).SetTextColor(System.Drawing.Color.Blue)); 
         
        }
    }
```
And thats all  it just put a HELLO WORLD notification on your screen :).