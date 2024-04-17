# Event Deploy for WPILib

A VSCode extension for quickly committing all changes before deploying robot code. Click "Deploy Robot Code (Event)" in the editor menu. The current branch _must_ begin with "event" (e.g. "event_nhgrs"). After an event, these commits can be squashed and merged to another branch.

This is intended for use with [AdvantageKit](https://github.com/Mechanical-Advantage/AdvantageKit). Replaying the code based on a log file requires that the same version of code is running in the simulator. We record the Git SHA as metadata in the log file; by making a new commit before every deploy, this extension guarantees that there are no uncommitted changes.

An example commit message is shown below.

> Deploy at "1/31/2022, 8:30:00 AM"

Modified from 6328's source due to a bug that prevented the extension from working on windows.
### Installation
Use the .vsix file to manually install in vscode.

### Updating Extension
To update the extension ensure you have Node.js installed then run the following command to install vsce.

```
npm install -g @vscode/vsce
```

With vsce installed, run the following command to generate a new .vsix file which can be used to update the extension in vscode.
```
vsce package
```