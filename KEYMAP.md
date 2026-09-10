# Toucan2 keymap

This document shows the key layout defined in `config/toucan.keymap`.

## Legend

- `tap / hold`: tap sends the first action; hold performs the second action.
- `---`: disabled key (`&none`).
- `▽`: falls through to the lower active layer (`&trans`).
- `C-Left`, `G-Left`: Control/GUI + arrow key.
- `Hyper`: Shift + Control + Alt + GUI.
- `Meh`: Shift + Control + Alt.
- Hold `Space / SYM` to enter SYM.
- Hold `Enter / NAV` to enter NAV.
- Holding NAV and SYM together enters ADJ.

## BASE — Dvorak

```text
 Left                                      Right
┌──────┬─────┬─────┬─────┬─────┬─────┐  ┌─────┬─────┬─────┬─────┬─────┬──────┐
│ Tab  │  '  │  ,  │  .  │  P  │  Y  │  │  F  │  G  │  C  │  R  │  L  │ Bspc │
├──────┼─────┼─────┼─────┼─────┼─────┤  ├─────┼─────┼─────┼─────┼─────┼──────┤
│ Ctrl │  A  │  O  │  E  │  U  │  I  │  │  D  │  H  │  T  │  N  │  S  │  -   │
├──────┼─────┼─────┼─────┼─────┼─────┤  ├─────┼─────┼─────┼─────┼─────┼──────┤
│Shift │  ;  │  Q  │  J  │  K  │  X  │  │  B  │  M  │  W  │  V  │  Z  │ Esc  │
└──────┴─────┴─────┴─────┴─────┴─────┘  └─────┴─────┴─────┴─────┴─────┴──────┘
              F16 / Hyper │ Space / SYM │ LANG2 / GUI
                          │ LANG1 / Alt  │ Enter / NAV │ F19 / Meh
```

## NAV

```text
 Left                                      Right
┌───────┬────────┬─────────┬────────┬─────────┬─────┐  ┌─────┬──────┬─────┬──────┬───────┬──────┐
│ Esc   │ C-Left │ C-Right │ G-Left │ G-Right │ --- │  │ --- │ ---  │ --- │ ---  │ ---   │ Bspc │
├───────┼────────┼─────────┼────────┼─────────┼─────┤  ├─────┼──────┼─────┼──────┼───────┼──────┤
│ Ctrl  │  ---   │   ---   │  ---   │   ---   │ --- │  │Home │ Left │ Up  │ Down │ Right │ End  │
├───────┼────────┼─────────┼────────┼─────────┼─────┤  ├─────┼──────┼─────┼──────┼───────┼──────┤
│ Shift │ Studio │    ▽    │   ▽    │    ▽    │  ▽  │  │  ▽  │  ▽   │  ▽  │  ▽   │   ▽   │  ▽   │
└───────┴────────┴─────────┴────────┴─────────┴─────┘  └─────┴──────┴─────┴──────┴───────┴──────┘
                  Alt │ Space / SYM │ LANG2 / GUI
                      │ LANG1 / Alt  │ Enter / NAV │ F19 / Meh
```

`Studio` is the ZMK Studio unlock action. Mouse and scroll-mode actions from the
older Toucan keymap are intentionally omitted.

## SYM

For the number row, tapping produces the number and holding produces its shifted
symbol (for example, tap `1`, hold `!`).

```text
 Left                                           Right
┌──────┬────┬────┬────┬────┬────┐  ┌────┬────┬────┬────┬─────┬──────┐
│ Tab  │ F1 │ F2 │ F3 │ F4 │ F5 │  │ F6 │ F7 │ F8 │ F9 │ F10 │ Bspc │
├──────┼────┼────┼────┼────┼────┤  ├────┼────┼────┼────┼─────┼──────┤
│ Ctrl │1/! │2/@ │3/# │4/$ │5/% │  │6/^ │7/& │8/* │9/( │0/)  │  =   │
├──────┼────┼────┼────┼────┼────┤  ├────┼────┼────┼────┼─────┼──────┤
│Shift │ `  │ [  │ ]  │ /  │ \\  │  │ ~  │ {  │ }  │ ?  │  |  │+/Shift│
└──────┴────┴────┴────┴────┴────┘  └────┴────┴────┴────┴─────┴──────┘
                  ▽ │ Space / SYM │ LANG2 / GUI
                    │ LANG1 / Alt  │ Enter       │ F19 / Meh
```

## ADJ — NAV + SYM

```text
 Left                                               Right
┌──────┬────────┬────┬────┬────┬────┐  ┌────┬──────┬──────┬──────┬───┬───┐
│ Tab  │ BT CLR │BT 0│BT 1│BT 2│BT 3│  │BT 4│Vol - │ Mute │Vol + │ ▽ │ ▽ │
├──────┼────────┼────┼────┼────┼────┤  ├────┼──────┼──────┼──────┼───┼───┤
│ Ctrl │   ▽    │ ▽  │ ▽  │ ▽  │ ▽  │  │ ▽  │ Prev │Play  │ Next │ ▽ │ ▽ │
├──────┼────────┼────┼────┼────┼────┤  ├────┼──────┼──────┼──────┼───┼───┤
│Shift │   ▽    │ ▽  │ ▽  │ ▽  │ ▽  │  │ ▽  │  ▽   │  ▽   │  ▽   │ ▽ │ ▽ │
└──────┴────────┴────┴────┴────┴────┘  └────┴──────┴──────┴──────┴───┴───┘
              F16 / Hyper │ Space / SYM │ LANG2 / GUI
                          │ LANG1 / Alt  │ Enter       │ F19 / Meh
```

`BT CLR` clears the current Bluetooth connection. `BT 0` through `BT 4` select
Bluetooth profiles.

## MOU

The existing MOU layer is unchanged. All main keys are transparent.

```text
                  Middle │ Left │ Right
                         │ Left │ Right │ Middle
```

There is no SCROLL layer in this keymap.
