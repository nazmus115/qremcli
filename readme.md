# qrem - The Minimalist CLI Task Scheduler

**qrem** is a lightweight, offline task scheduler and reminder tool for Windows. It runs entirely in your terminal (Command Prompt or PowerShell) and uses exactly **0 MB of RAM** in the background until the exact moment a notification pops up on your screen.

If you are tired of reminder apps that slow down your computer or require you to make an account, this is for you.

---

##  Features

* **Zero Background Bloat:** Uses native Windows Task Scheduler instead of heavy background processes.
* **100% Offline:** Everything stays on your local hard drive. No internet connection is required.
* **Native Desktop Alerts:** Pops up standard Windows notifications that you won't miss.
* **Frictionless Setup:** Comes with automated install and uninstall scripts. You don't need to be a programmer to set it up.

---

## How to Install

1. Download the latest `qrem-windows-v1.0.zip` file from the [official website](https://github.com/nazmus115/qremcli/releases/download/Stable/qrem-windows-v1.0.zip).
2. Right-click the `.zip` file and select **Extract All...** to unzip it.
3. Open the extracted folder and double-click the **`install.bat`** file.
* *Note: If Windows shows a blue "Windows protected your PC" popup, click **More info** and then **Run anyway**. This happens because the app is an independent, unsigned tool.*


4. A black window will appear, set everything up, and ask you to press any key to close it.
5. Close any open terminal windows you have, then open a fresh **Command Prompt** or **PowerShell**.

You are now ready to use `qrem`!

---

## How to Use

Open your terminal (press `Windows Key`, type `cmd`, and hit `Enter`) and type any of the following commands.

### 1. Add a New Reminder

To create a reminder, you need a Title, a Date/Time, and a Type (`one-time` or `daily`).
**Important:** You must put quotation marks `"` around the title and the date.

**For a one-time alert:**

```bash
qrem add "Finish my assignment" "2026-09-28 14:30" one-time

```

*(This will pop up a notification on Sept 28, 2026 at 2:30 PM)*

**For a daily repeating habit:**

```bash
qrem add "Practice C++ coding" "2026-09-29 10:00" daily

```

*(This will remind you every day at 10:00 AM, starting on Sept 29)*

### 2. View Your Schedule

To see a list of everything you have scheduled, type:

```bash
qrem list

```

This will print out a neat table showing the ID, Title, Time, and Type of all your active tasks.

### 3. Remove a Specific Task

First, type `qrem list` to find the **ID number** of the task you want to delete. Then type:

```bash
qrem remove 1

```

*(This deletes the task with ID 1)*

### 4. Delete All Tasks

If you want to completely wipe your schedule and start fresh, type:

```bash
qrem purge

```

### 5. Need Help?

If you ever forget a command, just type:

```bash
qrem --help

```

---

## How to Uninstall

If you ever want to remove `qrem` from your computer completely:

1. Go back to the folder where you extracted the original files.
2. Double-click the **`uninstall.bat`** file.
3. It will safely delete the database, remove the hidden background task, and clean up your computer.
