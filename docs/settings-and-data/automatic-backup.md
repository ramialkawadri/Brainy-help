# Automatic Backups

Brainy automatically creates regular backups of your entire database to protect against data loss.

## How Backups Work

### Backup Location
- Backups are stored automatically in your settings directory
- Same location as your main `brainy.db` database file

### Backup Naming
- Each backup includes a timestamp (e.g., `brainy.db.backup.2025-01-22-145030`)
- Timestamps help you identify when each backup was created
- Multiple backups accumulate over time

## Restoring from a Backup

If something goes wrong and you need to restore from a backup:

### Steps to Restore

1. **Close Brainy** — Exit the application completely

2. **Navigate to Settings Directory** — Locate your backups
   - Find the folder containing your `brainy.db` file
   - You'll see backup files named `brainy.db.backup.*`

3. **Select Your Backup** — Choose which backup to restore from
   - Pick the timestamp closest to when you last had good data

4. **Prepare for Restore**
   - Delete or rename the current `brainy.db` file (save it elsewhere as a safety measure)
   - Rename your chosen backup file to `brainy.db`

5. **Restart Brainy** — Open the application
   - It will load data from the restored backup

### Example
```
Original:  brainy.db.backup.2025-01-20-100000
Restore:   brainy.db
```

## Best Practices

- ✅ Enable auto-sync to keep cloud copies of your data
- ✅ Periodically backup your settings directory to external storage
- ✅ Note the timestamps of your most important backups
- ⚠️ Always keep the current `brainy.db` file as a safety measure before testing restores
