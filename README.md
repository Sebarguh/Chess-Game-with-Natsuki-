# Chess for Just Natsuki

Adds a **full game of chess** to Just Natsuki. Natsuki found an old chess set in the closet, practices alone until you walk in on her, and eventually challenges you to a game. She watches the board, **reacts to your moves** (captures, checks, blunders, comebacks...), gets better over time, and remembers how your games went.

> **Unofficial fan-made submod, in BETA.** Not affiliated with or supported by the Just Natsuki developers. Please report problems [here](../../issues), not to the JN Team.

> Part of Sebarguh's Unofficial Submods for Just Natsuki ([https://github.com/Sebarguh/Unofficial-JN-Submods-Hub](https://github.com/Sebarguh/Unofficial-JN-Submods-Hub)).

---

## Back up your persistent file first

This submod stores several small values in your persistent file (whether you saw the introduction, your win/loss history, which options are unlocked...). Back it up before installing, as you should for any submod.

1. Close the game.
2. Open your Ren'Py save folder (Windows: `%APPDATA%\RenPy\` · macOS: `~/Library/RenPy/` · Linux: `~/.renpy/`).
3. Open the Just Natsuki folder and copy the file named `persistent` somewhere safe.

Full instructions (including how to restore): [see the hub page](https://github.com/Sebarguh/Unofficial-JN-Submods-Hub#back-up-your-persistent-file).

---

## Features

- **A complete chess game** against Natsuki: all the standard rules (castling, en passant, promotion, check, checkmate, stalemate and the fifty-move rule), with legal moves enforced.
- **Play white, play black, or let Natsuki choose** her side. When you play black, the board is flipped so your pieces are at the bottom.
- **Pick up and place your pieces your way**: click a piece, or **grab it and drag it**. Legal squares light up. Placing a piece on a square only *previews* the move: nothing is played until you press **Play**, and you can press **Cancel** if you change your mind.
- **A real session**, in the style of the other JN games: Natsuki takes the box out of the closet, sets the pieces up on the table, and slides to the left while the board appears on the right. The board also stays on the table in front of her.
- **A one-time introduction** when the game is first unlocked: Natsuki, on a black screen, practicing against herself and thinking out loud, with the sound of the pieces moving. Then you "enter" and she notices you, flustered. She explains how chess works if you ask (or if you tell her you've never played), and invites you to play.
- **Natsuki reacts to the game**: first capture, pieces left hanging (yours, and sometimes hers!), threats, checks, castling, promotions, queens leaving the board, the endgame, material advantage, long games, how fast or slow you play, and more. Her lines change with your affinity level.
- **Progression**: at first she only plays the **Beginner** level (picked automatically, no menu). **30 days later**, she announces she has been practicing, and the **Intermediate** and **Expert** levels unlock.
- **She remembers**: wins, losses, draws, forfeits and streaks change what she says. After four losses in a row, she worries about you and ends the session.
- **Pause and Forfeit** buttons, and Natsuki reacts to both. While you are paused, she waits (and makes a comment if you take a while), then reacts when you come back.
- **The hand cursor from the headpats** appears when your mouse is over the board during your turn.
- **Sound effects** for grabbing, placing and moving pieces, captures, checks, castling and promotions (supply your own files, see below).
- **Highlights** for the selected piece, the possible squares, the move you are previewing, the king in check, and the last move (in a different color for yours and Natsuki's).
- Everything visual is **customizable** (colors, sizes, animations): see [Customization](#customization).

---

## How the game is unlocked

The submod follows the same philosophy as the other JN games: you have to earn it.

- Step ; What happens ; When 
- ---;---;---
- **1. Introduction** ; A one-time greeting at game launch, where Natsuki is found practicing chess on her own. ; **Snap and Blackjack unlocked**, and **at least 30 days** since your very first visit to the game.
- **2. The topic** ; **"Do you want to play chess?"** appears in the **Games** category of the talk menu (needs at least **Happy** affinity). ; After the introduction.
- **3. Beginner level** ; The only level at the start. It is chosen automatically. ; Right away.
- **4. Intermediate and Expert** ; Natsuki announces that she has improved, and the level menu appears. ; **30 days** after the introduction.

> JN does not record *when* Snap and Blackjack were unlocked, so the 30 days are counted from your first visit to the game. If you have been playing for a while already, you get the introduction on your next launch once both games are unlocked.

---

## How to play

1. Ask Natsuki **"Do you want to play chess?"** from the Games menu.
2. Pick your side (**White**, **Black**, or let **Natsuki** choose). White always moves first.
3. Natsuki sets up the board on the table (black screen, sounds), then slides to the left while the board appears on the right.
4. **Select a piece**: click it, or grab it and drag it. The squares it can move to light up.
5. **Place it** on a highlighted square (click the square, or drop the piece on it). The move is only *previewed*.
6. Press **Play** to confirm, or **Cancel** to start over.
7. Natsuki thinks, answers, and comments.

- Button ; What it does
- ---;---
- **Play** ; Confirms the move you are previewing.
- **Cancel** ; Forgets the selected piece and the previewed move.
- **Pause / Resume** ; Hides the board and stops the game. Natsuki notices and waits.
- **Forfeit** ; Gives up the game (Natsuki asks you to confirm, in her own way).

### Rules in short

- Standard chess rules, including castling, en passant and check/checkmate detection.
- Promotion is **always to a queen**.
- A game ends by checkmate, stalemate, the fifty-move rule, or a forfeit.

### Natsuki's levels

- Level ; How she plays
- ---;---
- **Beginner** ; Plays quickly and carelessly. Prefers captures, and sometimes leaves pieces hanging (she will deny it).
- **Intermediate** ; Looks one move ahead, with some randomness.
- **Expert** ; Looks two moves ahead and plays much more carefully.

> She is a small, simple chess engine, not a grandmaster. The goal is a fun game with a lot of personality.

---

## Installation

1. **Back up your persistent file** (see above).
2. Download the latest release.
3. Close the game.
4. Copy **`Chess_submod.rpy`** into your submods folder: `Just Natsuki/game/submods/` *(create it if it doesn't exist)*.
5. Copy the **`chess`** folder into `Just Natsuki/game/mod_assets/games/` *(create the folders if they don't exist)*, so that the files end up in `game/mod_assets/games/chess/`.
6. Launch the game. The first launch may take longer while Ren'Py recompiles.
7. The introduction plays on a launch where its conditions are met (see [How the game is unlocked](#how-the-game-is-unlocked)). After that, the topic appears in the Games menu.

> **The images and sounds are optional.** If a file is missing, the submod uses a fallback (a plain board with text symbols for the pieces, no sound, simple squares for the highlights...). It works without any asset, but looks much better with them.

### Files in `game/mod_assets/games/chess/`

**Images**

- File ; Size ; Used for
- ---;---;---
- `board_white.png` ; 474 × 474 px ; The board on the right when you play **white** (white at the bottom).
- `board_black.png` ; 474 × 474 px ; The board on the right when you play **black** (black at the bottom).
- `board.png` ; 474 × 474 px ; Fallback board for both sides, if the two files above are missing.
- `chess_board_desk_white.png` ; 1280 × 740 px ; The board lying on the table when you play white.
- `chess_board_desk_black.png` ; 1280 × 740 px ; The board lying on the table when you play black.
- `chess_board_desk.png` ; 1280 × 740 px ; Fallback table image for both sides.
- `wK.png`, `wQ.png`, `wR.png`, `wB.png`, `wN.png`, `wP.png` ; 56 × 56 px ; White pieces (king, queen, rook, bishop, knight, pawn).
- `bK.png`, `bQ.png`, `bR.png`, `bB.png`, `bN.png`, `bP.png` ; 56 × 56 px ; Black pieces.
- `chess_highlight.png` ; 56 × 56 px ; White rounded square, recolored by the submod for the highlights.

- The **board** is 474 × 474 px: an 8 × 8 grid of 56 px squares (448 px) with a **13 px frame** all around. The top-left square of the grid is a light square.
- The **table image** has the size of the whole screen area used by JN's desk items (1280 × 740 px). Transparent background, the board drawn at the center of the table. It is drawn in front of Natsuki and the table, and it follows her when she slides to the left.
- **Pieces** have a transparent background. Keep a few transparent pixels around each piece so it is not cropped when it grows or swings.
- You can draw everything at double size (board 948 × 948, pieces 112 × 112): the submod scales it.

**Sounds** (all optional, `.ogg`)

- File ; When
---;---
`chess_pieces_setup.ogg` ; The pieces are placed on the board (black screen).
`chess_piece_grab.ogg` ; You grab a piece.
`chess_piece_drop.ogg` ; You place a piece on a square (before pressing Play).
`chess_move.ogg` ; A move is played, by you or by Natsuki.
`chess_capture.ogg` ; A capture.
`chess_check.ogg` ; A check (or a checkmate).
`chess_castle.ogg` ; Castling.
`chess_promote.ogg` ; A promotion.

- When Natsuki takes the box out or puts the game away, the submod uses JN's own `drawer` sound, like the card game.
- A special sound (check, castling, promotion) falls back to `chess_move.ogg` if it is missing.

### Uninstalling

Close the game, delete `Chess_submod.rpy` from the submods folder and the `chess` folder from `mod_assets/games/`. If you want a fully clean state, restore your `persistent` backup. Otherwise the leftover values are harmless.

---

## Customization

Open `Chess_submod.rpy`: the settings are at the top of the file, each with a comment. Some of the most useful ones:

- Setting ; What it changes
- ---;---
- `CHESS_SQ` ; Size of a square, in pixels (default `56`). Redraw the pieces at the same size.
- `CHESS_FRAME` ; Thickness of the board frame (default `13`).
- `CHESS_COL_SELECTED`, `CHESS_COL_TARGET`, `CHESS_COL_PENDING`, `CHESS_COL_CHECK` ; Highlight colors: selected piece, possible squares, previewed move, king in check.
- `CHESS_COL_LAST`, `CHESS_COL_LAST_NATSUKI` ; Color of the last move, yours and Natsuki's.
- `CHESS_HL_ALPHA` ; Opacity of the highlights (`0.75` by default).
- `CHESS_BUTTON_W` ; Width of the buttons under the board (default `200`).
- `CHESS_HOVER_ZOOM`, `CHESS_GRAB_ZOOM` ; How much a piece grows when hovered / grabbed.
- `CHESS_WOBBLE_ANGLE`, `CHESS_WOBBLE_TIME`, `CHESS_WOBBLE_PIVOT` ; The swing of a grabbed piece, like a chandelier.
- `CHESS_PAUSE_IDLE_TIMES` ; When Natsuki comments while you are paused. Use `()` to keep her silent.
- `CHESS_INTRO_REQUIRED_DAYS` ; Days since your first visit before the introduction (default `30`).
- `CHESS_LEVELS_REQUIRED_DAYS` ; Days after the introduction before Intermediate and Expert unlock (default `30`).
- `CHESS_CURSOR_IMG`, `CHESS_CURSOR_HOTSPOT` ; The hand cursor shown over the board.

### Testing the introduction and the levels

- Set `CHESS_INTRO_REQUIRED_DAYS` and `CHESS_LEVELS_REQUIRED_DAYS` to `0` to skip the waiting.
- Set `CHESS_DEBUG_FORCE_INTRO = True` to replay the introduction **at every launch**. **Put it back to `False` afterwards.**

---

## What is saved in your persistent file

- Value ; Purpose
- ---;---
- `_jn_chess_intro_seen`, `_jn_chess_intro_pending`, `_jn_chess_intro_date` ; The introduction has been (or is about to be) played, and when.
- `_jn_chess_levels_announced` ; Natsuki already announced the new levels.
- `_jn_chess_rules_offered`, `_jn_chess_explanation_given` ; The rules / controls have already been offered or explained.
- `_jn_chess_memory` ; Games started and completed, wins, losses, draws, forfeits, streaks and the last result.
- `_jn_chess_greeting_database` ; The registration of the introduction greeting.

- ---

## How it works (for submod makers)

The submod hooks into JN without editing any of its files, and everything lives in a single `.rpy` file (the chess rules and the small AI are included).

- It registers the topic `talk_play_chess` in the **Games** category, with the conditional `chess_topic_unlocked()` and a minimum affinity of Happy.
- It registers the greeting `greeting_chess_intro` (as `TOPIC_TYPE_GREETING`), and wraps `jn_events.selectEvent()` and `jn_greetings.selectGreeting()` so the introduction takes the first normal greeting slot once it is pending. Vanilla special greetings keep priority.
- It wraps `Natsuki.calculatedAffinityGain()` so that clicking the topic doesn't give affinity by itself: only a *completed* game does.
- It wraps `quitInputCheck()`, so leaving in the middle of a game counts as a sudden leave.
- The board on the table is a JN desk item set in the **centre** slot, with `Natsuki.setDeskItem()`.
- The hand cursor is set the same way the Headpats extra does it, through `config.mouse`, and reset when the mouse leaves the board.
- The highlights are one white image recolored with `im.Recolor`, so it works on Ren'Py 6.99.
- Natsuki's expressions only use sprite codes that already exist in the base game.
- Unlock conditions use `persistent.jn_snap_unlocked`, `persistent._jn_blackjack_unlocked` and `persistent.jn_first_visited_date`.
- The persistent file is written to disk (`renpy.save_persistent()`) as soon as the introduction starts, so a sudden shutdown can't make it play twice. The introduction is also considered seen as soon as *any* sign of it exists (flag, date, a game already started...), and a missing flag is repaired.

---

## Known limitations (beta)

- **Compatibility is only tested on Just Natsuki `[1.3.5]`** (Ren'Py 6.99.12). Other versions may behave differently.
- **Possible conflicts with other submods** that change the greeting selection, the event selection, the affinity gain, or the same desk slot. Compatibility has not been systematically tested. If something looks wrong, remove one of them.
- **The chess AI is simple.** It looks at most two moves ahead, so a good player will beat it, and it can still make odd decisions at the lower levels (on purpose, for Beginner).
- **No promotion choice**: pawns always become queens.
- **Draws are limited**: stalemate and the fifty-move rule only. There is no draw by repetition or by insufficient material, and no way to offer a draw (use Forfeit).
- **A game can't be resumed.** If you close the game in the middle of a session, the position is lost (and it counts as a sudden leave).
- **Natsuki reacts mostly to situations** (captures, checks, threats...), not to specific chess openings or tactics.
- **Dialogues are in English only.**
- **The submod has mostly been tested at high affinity.** Her lines adapt to the Happy, Affectionate, Enamored and Love tiers, but the lower levels have seen far less testing.
- **Tested on Windows only for now.**

## Roadmap

These are ideas, not promises.

- [ ] **Major:** test every affinity level and fix what breaks
- [ ] **Major:** choice of the piece for promotion
- [ ] **Minor:** draw by repetition and by insufficient material
- [ ] **Minor:** a list of the moves played and the captured pieces
- [ ] **Minor:** resume an interrupted game
- [ ] **Minor:** more reactions, more variants, and comments on specific openings

Suggestions are welcome: open an issue.

---

## Reporting a bug

Please include:

1. Your Just Natsuki version and the other submods you have installed.
2. What you did, what you expected, and what happened.
3. The `traceback.txt` / `log.txt` from the game folder, if there is one.

## Transparency: AI assistance

The **structure and code** of this submod were written with the help of an AI assistant. The **dialogues, the expressions, Natsuki's tone and the visual design** were kept as faithful as possible to her character, and were written, reviewed and modified by me.

## Credits

- The team Salvato for Doki Doki Literature Club.
- The [Just Natsuki Team](https://github.com/Just-Natsuki-Team/NatsukiModDev) for the game and its source.
- The author of the **Ichi** (https://github.com/Zhaumbie/Ichi-for-Just-Natsuki) submod, whose game session and introduction greeting inspired the structure of this one.
- [Wowm](https://github.com/wowm03) for beta testing.
- You, for the support :>
"# Chess-Game-with-Natsuki-" 
