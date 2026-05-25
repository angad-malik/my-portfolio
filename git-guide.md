# An Absolute Beginner's Guide to Git: How to Fix the "Command Not Recognized" Error

You just installed Git, opened your terminal with excitement, typed your very first command, and hit Enter. Instead of a success message, a giant wall of red text slams your screen: 

`The term 'git' is not recognized as the name of a cmdlet...`

It is incredibly frustrating, but this error is a standard rite of passage for almost every software developer. It simply means Windows does not know where your Git installation folder is hiding yet.

This step-by-step guide helps you troubleshoot the error and connects Git to your terminal in less than five minutes.
## Solution 1: Check If Git is Actually Installed

Before you touch any environment variables, check if Windows actually finished downloading the program. Sometimes, a setup wizard closes without completing the background configuration.

1. Open your **Windows File Explorer**.
2. Navigate to this exact folder path: `C:\Program Files\Git`
3. Check for the executable files inside.

If you **do not see** a folder named `Git` there, the solution is simple: your installation didn't register. Head over to [git-scm.com](https://git-scm.com/download/win) and download the **64-bit Git for Windows Setup**. Run the installer, leave all the default settings checked, and click **Next** until it finishes.
## Solution 2: The "Golden Rule" of Terminals (The Restart)

If you checked your folders and Git is definitely installed, but your terminal still shows the "Not Recognized" error, you are likely hitting the most common beginner trap: **working in an outdated terminal session.**

Terminals are like old school registers—they only load your system paths when they first turn on. If you install Git while VS Code is already open, the terminal inside VS Code has no idea that Git now exists on your laptop.

### How to fix it:
1. Look at the top-right corner of your terminal panel in VS Code.
2. Click the **Trash Can icon** (Kill Terminal) to close the active, broken session.
3. Open a brand new terminal by pressing `Ctrl + ~` (or go to **Terminal** > **New Terminal** at the top menu).

When the new terminal opens, type `git --version` and hit Enter. 

Because you forced the terminal to refresh, it will now successfully look at your updated Windows system and print out your active Git version, like this:
`git version 2.54.0.windows.1`

---

> 💡 **Summary:** Never run an installer and expect an already-open terminal to read it. Always kill the terminal panel and open a fresh one to update your environment paths!