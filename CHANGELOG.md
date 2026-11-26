# Changelog

## 0.1.0 (364)

- A panel above the message box shows what a Claude session runs in the background, such as a long command or a subagent: what each task does, how long it has been running, and a button that stops only that task. `compagnion session stop-task <session> <task-id>` does the same from the command line.
- Stop in the message box now stops only the turn; background tasks keep running until they finish or you stop them in the panel.

## 0.1.0 (363)

- **Send now** works in Codex sessions that use subagents. Once a subagent had started, sending a queued message into the running turn failed with "expected active turn id … but found …", and Stop could fail the same way. A subagent finishing no longer ends the session's turn early either.

## 0.1.0 (362)

- Claude sessions work again. Since the switch to the Claude Agent SDK in 0.1.0 (361), every Claude session stopped at its first message with "Operation aborted" or "SharedArrayBuffer is not defined": the Claude runtime in the app was signed without the entitlements it needs to run.

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
