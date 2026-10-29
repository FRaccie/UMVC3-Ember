# UMvC3 Ember Netplay

Rollback netplay and online rooms for **Ultimate Marvel vs. Capcom 3** (Steam, PC).

This repository only hosts the downloads. **Test builds:** they can crash or desync. Crash reports are sent
automatically (see [Reports](#reports)).

## Download

Get the latest build from [Releases](../../releases):

- **Nightly** (pre-release): the newest test build, rebuilt with each change. A nightly plays online for 7 days after
  it was built; after that, download the latest one.
- `umvc3-ember-<version>-setup.exe`: the installer (recommended).
- `umvc3-ember-<version>.zip`: the same files, to extract yourself.
- `umvc3-ember-<version>-SHA256SUMS.txt`: checksums of both.

## Install

**Installer:** run the setup. It installs into its own folder (no administrator needed) and adds
"UMvC3 Ember Netplay" to the Start menu. Nothing is put in the game's folder.

**Zip:** extract every file into a folder of your own (not the game's folder) and start `umvc3-ember-launcher.exe`.

The launcher finds the game through Steam. If it does not, start it with the game's folder:

```
umvc3-ember-launcher.exe --game "D:\SteamLibrary\steamapps\common\ULTIMATE MARVEL VS. CAPCOM 3"
```

Older test builds were installed in the game's folder (`dinput8.dll` beside `umvc3.exe`). The installer removes that
one; with the zip, delete `dinput8.dll`, `umvc3-net.exe` and `crashpad_handler.exe` from the game's folder yourself.

Antivirus programs can flag unsigned mods. If the game will not start, add an exception for Ember's folder.

## Play

Start **UMvC3 Ember Netplay** (the launcher) with Steam running; it starts the game. Starting the game from Steam
starts it without Ember. The room board opens over the title screen; **F1** shows and hides it, **F10** shows the
game's own menus.

| | |
|---|---|
| Make a room | The invitation goes to your clipboard. Send it to the people you want to play. |
| Join | Copy an invitation, then press "Join from the clipboard". |
| Sit down / Queue | Take a seat at a battle table, or wait in its queue. The next two in the queue play. |
| Ready | When both seated players are ready, the game starts by itself. |
| Watch | Watch a table's games. |

A set is first to 2; the winner stays, the loser goes to the back of the queue.

During a fight the board hides; **F1** brings it back. **F5** shows or hides the netplay panel: ping, link, input
delay, rollbacks and the state checks between both games.

## Your files

Your settings, team and logs are in `%APPDATA%\umvc3e` (type that in Explorer's address bar). Include
`umvc3-ember.log` when you report a problem.

## Reports

When the game crashes, a crash report (a minidump of the game's memory and `umvc3-ember.log`) is sent to the
developers' error tracker. Problems such as a desync are reported too. To turn reports off, create an empty file named
`umvc3-ember-no-reports.txt` in `%APPDATA%\umvc3e`.

## Uninstall

**Installer:** uninstall "UMvC3 Ember Netplay" from Windows' Apps & features.
**Zip:** delete its folder. `%APPDATA%\umvc3e` holds your settings and logs; delete it too if you want them gone.

---

Ultimate Marvel vs. Capcom 3 is © CAPCOM and MARVEL. This project is not affiliated with or endorsed by either.
