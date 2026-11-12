<img src="icon.png" width="96" alt="Sideslate icon">

# Sideslate

Sideslate turns an old Android tablet or phone into a live dashboard for your Windows PC, over your own Wi-Fi.

Put the tablet next to your monitor and choose the tiles you want: CPU, GPU and RAM load, GPU temperature, FPS of the
game you're playing, top processes, what's playing in Spotify or the browser, your game time this week, plus a clock,
calendar, weather, notes, a timer and stock prices. The clock, calendar, weather, notes and timer also work when the PC
is off.

**Status: early beta.** Expect rough edges, and please [report them](https://github.com/sideslate/sideslate/issues).

## Download

Get the newest version from **[Releases](https://github.com/sideslate/sideslate/releases/latest)**.

| File | For |
|---|---|
| `Sideslate-PC-<version>-windows-x64.zip` | **Sideslate PC**, for the PC you want to watch (Windows 10 or 11, 64-bit) |
| `Sideslate-<version>-android.apk` | **Sideslate** for the tablet or phone (Android 6.0 or later, 32-bit devices too) |
| `Sideslate-Display-<version>-windows-x64.zip` | **Sideslate** for a second Windows device used as the dashboard |
| `*-linux-x64.tar.gz` | Experimental Linux builds, never run on a real Linux desktop |

Nothing else has to be installed; .NET is included in every download.

## Install

1. **On the PC:** unzip `Sideslate-PC` into a folder where it can stay, and start `SideslatePC.exe`.
   - Windows may say "Windows protected your PC", because the file is not signed yet. Choose **More info**, then
     **Run anyway**. Compare the file with `SHA256SUMS.txt` on the release page if you want to be sure it's the
     original.
   - Allow it when the firewall asks (private networks are enough).
   - No window opens. Sideslate PC runs in the background with an icon next to the clock (maybe behind the **^**
     arrow). Right-click the icon to quit.
2. **On the tablet or phone:** open the `.apk` and allow installing from this source when Android asks.
3. **Open Sideslate.** It searches for your PC by itself. Tap your PC when it appears and type the code that pops up on
   the PC. Both devices must be on the same Wi-Fi.

No PC? Choose **Use without a PC** and use the clock, calendar, weather, notes and timer on their own.

## If the PC is not found

- Check that Sideslate PC is running (its icon is next to the clock) and that the firewall allowed it.
- Guest Wi-Fi networks often stop devices from seeing each other. Use your main network.
- Some networks block the search. On the tablet, choose **Enter the PC's address** and type the address that the PC
  shows when you right-click the Sideslate PC icon (for example `192.168.1.20`).

## FPS counter (optional)

The FPS tile uses Intel's open-source PresentMon, which comes with Sideslate PC and only runs while an FPS tile is on a
connected tablet. Windows needs a one-time permission: right-click the Sideslate PC icon, choose
**Allow FPS counter...**, approve the administrator prompt, then sign out of Windows and back in. Some games with
anti-cheat software block this kind of reading; nothing is injected into the game.

## Privacy and security

- Everything stays on your own network. There is no account, no cloud service and no telemetry.
- Sideslate only goes to the internet for the tiles you add: weather (Open-Meteo), stock and crypto prices (Yahoo
  Finance), GitHub (the developer tiles), and the addresses you type into the Ping and API health tiles.
- A tablet has to be paired with a code shown on the PC before it can see anything.
- The connection inside your network is plain HTTP, so don't use it on a network you don't trust.

## Uninstall

- **PC:** right-click the Sideslate PC icon, untick **Start with Windows**, choose **Quit**, and delete the folder.
  Paired tablets, game time and logs are in `%APPDATA%\PcAgent1`; delete that folder too to remove everything.
- **Tablet or phone:** uninstall the Sideslate app.

## Feedback

Found a bug or missing something? [Open an issue](https://github.com/sideslate/sideslate/issues/new/choose). Please
say which release you downloaded; Sideslate PC also shows its version at the top of its icon's menu.

Sideslate is free to use. The source code is not public; this repository holds the downloads and the issue tracker.
