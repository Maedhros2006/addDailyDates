#!/bin/bash

# File to modify
filename="/Your/file/path/note.md"

# Current date in the format [[YYYY-MM-DD]]
current_date=$(date +"[[%Y-%m-%d]]")

# Check if the date is already present in the file
if ! grep -qF "$current_date" "$filename"; then
    # If the date is not found, append it to the file
    echo "$current_date" >> "$filename"
    echo "Added current date $current_date to the file."
else
    echo "Current date $current_date is already in the file."
fi
