# 💾 Backup Guide - Резервное копирование

## 🔄 Автоматическое резервное копирование

### Скрипт бэкапа проектов:
```bash
#!/bin/bash
BACKUP_DIR="/home/$USER/Backups"
PROJECTS_DIR="/home/$USER/Проекты"
DATE=$(date +%Y%m%d_%H%M%S)

# Создать папку для бэкапов
mkdir -p $BACKUP_DIR

# Создать архив проектов
tar -czf "$BACKUP_DIR/projects_backup_$DATE.tar.gz" "$PROJECTS_DIR"

echo "✅ Бэкап создан: $BACKUP_DIR/projects_backup_$DATE.tar.gz"
