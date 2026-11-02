# ascii-sharks

A Claude Code mod that adds a pane of animated ASCII sharks and fish beside the chat, in the Claude desktop app's Code tab or in the terminal. The pane opens when a session starts; run `/sharks` to open it again.

The animation is the simulation and shape rendering from [stackedlol/ascii-sharks](https://github.com/stackedlol/ascii-sharks) (MIT, see LICENSE), drawn as coloured text cells instead of on a canvas, so it is lower resolution than the web demo. `hooks/shark-view.js` is an unminified bundle of that code plus a small text-drawing layer.

## Install

In a Claude Code session, at the prompt:

```
/plugin install ascii-sharks --marketplace <your-github-username>/<your-repo-name>
```

Answer `y` to add the marketplace, then pick a scope. From a shell, the same thing is `claude plugin install ascii-sharks --marketplace <your-github-username>/<your-repo-name>`. Start a new session afterwards if the pane does not appear.

## Change the sharks

Edit the `SHARKS` list at the top of `hooks/register.tsx`. The kinds are classic, hammerhead, zebra, tiger, greathammer, mako, thresher and nurse; the first is the biggest and the sizes are relative to it.

## Needs a screen that draws panes

The pane only shows where a Claude Code screen is attached to the session (the desktop app's Code tab, or a terminal). In a plain claude.ai chat it has nowhere to draw. If `/sharks` says no screen is drawing the pane, that is why.
