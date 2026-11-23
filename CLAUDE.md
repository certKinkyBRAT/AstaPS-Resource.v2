# Notes for Claude

## Where changes go (owner's rule)

This repository is a personal fork: `emeliaMTF/AstaPS-Resource`. The original is `MeChen618/AstaPS-Resource`.

- Commit and push only to this fork. Open pull requests only against this fork's own `main` branch.
- Never push to, open pull requests on, open issues on, or comment on `MeChen618/AstaPS-Resource`, the upstream AstaPS server, or any repository other than the owner's forks.
- If a fix seems worth sharing upstream, tell the owner and let them ask the original creators first.

The matching server fork is `emeliaMTF/AstaPS-QuestVibe`, and the same rule applies there.

## Project notes

- Game data for the AstaPS 7.2 server. Quest definitions are in `ExcelBinOutput/QuestExcelConfigData.json` and `BinOutput/Quest/<mainId>.json`. Scene Lua scripts are in `Scripts/Scene/<sceneId>/`.
- Many quests carry a flattened `QUEST_COND_STATE_EQUAL [0, 3]` ("quest 0 finished") placeholder where the real prerequisite was lost. Restore real gates in `QuestExcelConfigData.json`, following earlier fixes such as Amber's 48101 and Kaeya's 46101.
- `QuestExcelConfigData.json` is very large. Edit it with exact text replacement, then check that it still parses as JSON.
- The owner has little coding experience. Explain findings and changes in plain language.
