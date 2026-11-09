# Changelog

## 0.1.0 (139)

- Updating by itself works for the notarized app: macOS's App Management protection no longer stops Compagnion from replacing itself with a newer release.
- Updating by itself shows only a small notice in the corner, "Updating to …" and what it waits for, without buttons. The buttons come back when the restart fails, or when *Restart automatically on update* is off.
- Clearer descriptions of the update settings, and the update steps in Console (subsystem `email.boots.compagnion`, category `update`).

## 0.1.0 (137)

The first public release.

- Workspaces as git worktrees, each with its own branch, for Claude Code and Codex.
- Approvals, attachments and a context meter in the chat.
- The changes of every turn, with a diff per turn and revert.
- Pull requests from the app: a model writes the description, checks and merge in a bar above the right panel.
- A dashboard with a column per status, and a command palette (⌘K).
- Setup and run scripts, actions and terminals per repo, with a preview of localhost addresses.
- The `compagnion` command-line tool in the app bundle.
- Updates itself from the releases in this repository, checking the checksum and the Developer ID signature of every update.
