# Run `.sh` Files in Konsole on Double-Click (KDE Dolphin)

By default, Dolphin opens `.sh` files in an editor instead of executing them.
This guide shows how to configure Dolphin so that **double-clicking any `.sh` file runs it inside Konsole**.

## Step 1 — Make `.sh` Files Executable

There are two ways:

**From the GUI (recommended for beginners):**

1. Right-click the `.sh` file → **Properties**.
2. Go to the **Permissions** tab.
3. Check the box **Is executable** (or **Allow executing file as program**).
4. Apply and close.

**From the terminal (one-liner):**

```bash
chmod +x your_script.sh
```

## Step 2 — Configure Dolphin’s Behavior

1. Open **Dolphin → Settings → Configure Dolphin**.
2. Go to the **Confirmations** section.
3. Under **When opening an executable file**, select:

   * ✅ **Open in Application**

This tells Dolphin to actually run executables when double-clicked, instead of just opening them in a text editor.


## Step 3 — Set Default Application for `.sh` Files

1. Right-click any `.sh` file → **Properties**.
2. In the **General** tab, click **Change…** next to “Opens with”. 
3. In the dialog, click **Add…** and enter:

   ```
   konsole -e
   ```
         
4. Move this entry to the **top of the Application Preference Order**. 
5. Apply and close.


P.S. I’ve added a simple script to test this
