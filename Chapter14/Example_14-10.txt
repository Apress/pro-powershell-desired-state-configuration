#!/bin/bash
message=$(git log -1 --format=%s)

exec powershell.exe -NoProfile -ExecutionPolicy Bypass -File "$PWD/.git/hooks/post-commit.ps1" -CommitMessage "\'$message\'"