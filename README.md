# Goalkeeper Simulator

Developed by **CYFRON SOFTWARE TRADING**.

A browser game where you are taking on responsibilities of the goalkeeper. A real shot is struck at your goal, and you have a fraction of a second to pick where to dive.

Every shot comes from a real match: the shooting position and the point where the ball reached the goal are taken from World Cup, Euro, Champions League, La Liga, Bundesliga and Copa América games. In penalty mode you face real penalties by Messi, Ronaldo, Kane and others, and you see each taker's habits before the kick.

The whole game is a single HTML file. It needs no installation, no build step and no server code, and it plays on phones, tablets and computers.

**Play it here:** `https://deminalexeys.github.io/Goalkeeper-simulator/`

Languages: English, French, Russian.

---

## How to play

### The goal

The goal is split into six zones: three columns (left, centre, right) and two rows (top, bottom).

```
+-----------+-----------+-----------+
| top left  | top centre| top right |
+-----------+-----------+-----------+
|bottom left|bottom ctr.|bottom rght|
+-----------+-----------+-----------+
```

When the ball is struck, choose the zone it is heading for. Save as many of the 10 shots in a series as you can.

### A shot, step by step

1. **Get ready.** You see the shot type, the distance and the angle (for example "Free kick, 22 m, 13° right"). The small pitch map in the bottom-left corner shows where the shooter stands. In penalty mode you also see who is taking it and where their penalties usually go.
2. **Shot!** The ball is kicked. Only now does your input count; tapping before the kick does nothing.
3. **Dive.** Choose a zone while the ball is in the air. Only your first choice counts.
4. **Result.** Save or goal, why it happened, the ball speed, the flight time, your reaction time, and what happened in the real match.

### When is it a save?

Two things must be true:

- **Right place.** The ball must arrive inside the zone you chose. You also reach about 30 cm beyond its edges, so a ball just outside your zone can still be saved.
- **In time.** A dive to the left or right needs a moment to get there, so you have to choose a corner zone a little before the ball arrives. The centre zones need no extra time. How much extra time a corner needs depends on the speed setting (see below). If you pick the right corner too late, it is a goal, and the result tells you how early you needed to be.

If you don't choose anything before the ball arrives, it is a goal.

### Controls

| Device | How to dive |
|---|---|
| Phone or tablet | Touch the part of the screen that matches the zone: left, middle or right, above or below the middle of the goal. You don't have to hit the goal itself, the whole screen works. |
| Mouse | Click a zone. |
| Keyboard | `Q` `W` `E` for the top zones, `A` `S` `D` for the bottom zones. On a French AZERTY keyboard, use the keys in the same positions: `A` `Z` `E` and `Q` `S` `D`. `Space` or `Enter` moves to the next shot. |

The game plays best with a phone turned sideways.

### Game modes

| Mode | What you face |
|---|---|
| **Open play** | A mix of free kicks and shots from outside the box. Free kicks dip and curl; open-play shots are faster and flatter. You have time to read the flight. |
| **Penalties** | Real penalties from 11 m. Before each kick you see where that player's other penalties went. At real speed, a penalty save is usually a guess, just as it is for real keepers. |

### Ball speed

| Setting | Ball speed | Extra time a corner dive needs |
|---|---|---|
| Slow | 60% of real speed | none |
| Medium | 80% of real speed | 0.08 s |
| Real life | real speed | 0.16 s |

Start on Slow to learn how the shots fly, then move up.

### Review after each shot

With **"Pause and review after every shot"** ticked, the game stops after each shot and explains the result. Untick it to play all 10 shots back to back and see the full review at the end.

### End of the series

After 10 shots you see:

- how many shots you saved,
- your average reaction time,
- your best run of saves in a row,
- the zone you conceded most often,
- a table of every shot: where the ball went, where you dived, your reaction time and the result.

Your best score is saved separately for each mode and speed setting. **Replay level** plays the same 10 shots again, so you can see whether you improve.

### Other options

- **Language:** the EN / FR / RU buttons in the top-right corner of the menu. The game starts in English and remembers your choice.
- **Sound:** the speaker button at the top of the screen during play. On an iPhone, sound only plays when the side silent switch is off.
- **Custom background:** pick any photo from your device to use as the stadium behind the goal. It stays on your device and is not uploaded anywhere.

Records, language and sound settings are stored only in your browser. Clearing the browser's site data resets them.

---

## Running and deploying the game

The game is the single file `index.html`. It has no dependencies. It uses an internet connection only to load its font; without one, it falls back to the device's standard font and works the same.

### Publish it with GitHub Pages (recommended)

1. Put `index.html` and this `README.md` in the root of the repository.
2. Open the repository on GitHub and go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Choose the `main` branch and the `/ (root)` folder, then click **Save**.
5. Wait a minute or two. The page shows the game's address, in the form `https://<your-username>.github.io/<repository-name>/`.

Open that address on any phone or computer to play, and share it with anyone. Every time you push a new version of `index.html`, the site updates by itself within a few minutes.

The file must be named `index.html` for the game to open at the main address. With any other name, you add the file name to the end of the address.

### Play on a computer without publishing

Download `index.html` and double-click it. It opens in your browser and plays from your own computer.

### Phones

Open the published web address in the phone's browser. A downloaded HTML file does **not** work on iPhone: the Files app shows a preview of the page but doesn't run the game, so the buttons do nothing. Use the GitHub Pages address instead.

---

## Data and credits

- **Developer:** CYFRON SOFTWARE TRADING
- **Shot data:** [StatsBomb Open Data](https://github.com/statsbomb/open-data). Check StatsBomb's terms in that repository before publishing; they ask public projects that use the data to credit StatsBomb.
- **Ball speed** is not in the data, so it is estimated from published research: penalties 65–105 km/h, free kicks 72–90 km/h, open-play shots 80–112 km/h.
- **Flight path:** the dip and curl of each shot are reconstructed between the real shooting position and the real point where the ball reached the goal.
- Player and team names are shown as they appear in the source data.
- Sound effects are generated by the game's code; there are no audio files.
