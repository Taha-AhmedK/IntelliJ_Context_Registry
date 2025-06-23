# 🖱️ Open with IntelliJ IDEA - Windows Context Menu Integration

This Windows Registry script adds **"Open with IntelliJ IDEA"** to the right-click context menu for:

- Folder background (empty space inside a folder)
- Folders (when right-clicked directly)
- Files (any file type)


## 🛠️ How to Use

1. Open a text editor (like Notepad).
2. Paste the contents of the `.reg` file (see below).
3. Save the file as `intellij-context-menu.reg`.
4. Double-click the file and confirm the changes to the Windows Registry.

## 📄 Registry Script (📌 Note: Update the path to match your IntelliJ installation directory if it's different)

```
Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\Directory\Background\shell\Open with IntelliJ IDEA]
@="Open with IntelliJ IDEA"
"Icon"="\"C:\\Program Files\\JetBrains\\IntelliJ IDEA Community Edition 2025.1\\bin\\idea64.exe\""

[HKEY_CLASSES_ROOT\Directory\Background\shell\Open with IntelliJ IDEA\command]
@="\"C:\\Program Files\\JetBrains\\IntelliJ IDEA Community Edition 2025.1\\bin\\idea64.exe\" \"%V\""

[HKEY_CLASSES_ROOT\Directory\shell\Open with IntelliJ IDEA]
@="Open with IntelliJ IDEA"
"Icon"="\"C:\\Program Files\\JetBrains\\IntelliJ IDEA Community Edition 2025.1\\bin\\idea64.exe\""

[HKEY_CLASSES_ROOT\Directory\shell\Open with IntelliJ IDEA\command]
@="\"C:\\Program Files\\JetBrains\\IntelliJ IDEA Community Edition 2025.1\\bin\\idea64.exe\" \"%1\""

[HKEY_CLASSES_ROOT\*\shell\Open with IntelliJ IDEA]
@="Open with IntelliJ IDEA"
"Icon"="\"C:\\Program Files\\JetBrains\\IntelliJ IDEA Community Edition 2025.1\\bin\\idea64.exe\""

[HKEY_CLASSES_ROOT\*\shell\Open with IntelliJ IDEA\command]
@="\"C:\\Program Files\\JetBrains\\IntelliJ IDEA Community Edition 2025.1\\bin\\idea64.exe\" \"%1\""
```