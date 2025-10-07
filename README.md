
                        RDS SESSION MANAGER v4.0


DESCRIPTION
-----------
RDS Session Manager is a powerful and user-friendly tool designed for IT 
administrators to manage Remote Desktop sessions on Windows Terminal Servers. 
This application provides a centralized interface to monitor, connect to, and 
control user sessions across multiple RDS servers.


KEY FEATURES
------------

• Multi-Server Management
  - Quick server switching via dropdown menu
  - Custom server list management (add/edit/delete servers)
  - Server configurations saved between sessions

• Session Monitoring
  - Real-time session status display (Active/Disconnected)
  - User-friendly visual indicators (green for active, gray for disconnected)
  - Session count statistics (total, active, disconnected)
  - Live search/filter functionality for quick user lookup

• Session Control
  - One-click connection to user sessions with shadow mode
  - Safe session termination (logoff) with confirmation prompt
  - Double-click quick connect
  - Right-click context menu for quick actions

• User Interface
  - Bilingual support (English/Russian) with instant language switching
  - Keyboard shortcuts for power users:
    * F5 - Refresh session list
    * Enter - Connect to selected session
    * Delete - Logoff selected session
    * Escape - Deselect session
  
• Advanced Features
  - Auto-refresh mode (updates every 30 seconds)
  - Multi-threaded session loading (non-blocking interface)
  - Real-time search filtering
  - Status bar with last update timestamp
  - About window with developer information and donation options


SYSTEM REQUIREMENTS
-------------------
• Operating System: Windows 10/11 or Windows Server 2016+
• Python 3.7 or higher (if running from source)
• Network access to target RDS servers
• Appropriate permissions to query and manage remote sessions
• Administrator rights may be required for session shadowing


INSTALLATION
------------
1. Download or extract the file RDS_SM_v4.0.exe from the archive
2. Run the file, then choose whether to install the program for yourself 
   or for all users on the PC
3. Leave the default installation directory or select your own
4. Wait for the installation to complete and choose to create a desktop 
   shortcut
5. Find the shortcut on your desktop and launch the program


FIRST TIME SETUP
----------------
1. Launch the application
2. Click the gear icon (⚙) next to the server dropdown
3. Add your RDS server names or IP addresses
4. Click "Save" to store the server list
5. Select a server from the dropdown
6. Click "Refresh (F5)" to load sessions


USAGE
-----

Connecting to a Session:
  1. Select a server from the dropdown menu
  2. Select a user session from the list
  3. Double-click or press Enter to connect
  4. A Remote Desktop window will open in shadow mode with control

Terminating a Session:
  1. Select a user session from the list
  2. Click "Logoff (Del)" or press Delete key
  3. Confirm the action in the dialog
  4. The session will be safely terminated

Managing Servers:
  1. Click the gear icon (⚙) next to the server selector
  2. Use Add/Edit/Delete buttons to manage your server list
  3. Double-click a server name to quickly edit it
  4. Changes are automatically saved

Language Switching:
  - Click "ENG" for English interface
  - Click "RUS" for Russian interface
  - Your preference is saved automatically


CONFIGURATION FILES
-------------------
The application creates two configuration files in its directory:

• servers.json
  Contains your list of RDS servers
  Format: ["SERVER1", "SERVER2", "SERVER3"]

• language.json
  Stores your preferred interface language
  Format: {"language": "eng"} or {"language": "rus"}

These files can be manually edited with any text editor if needed.


TROUBLESHOOTING
---------------

Problem: "Failed to get data from server"
Solution: 
  - Verify the server name or IP address is correct
  - Ensure you have network connectivity to the server
  - Check if you have permissions to query remote sessions
  - Try using IP address instead of hostname

Problem: Cannot connect to user session
Solution:
  - Verify Remote Desktop Services are running on the target server
  - Ensure you have shadow connection permissions
  - Check Windows Firewall settings on both local and remote machines
  - Verify Group Policy allows session shadowing

Problem: Sessions list is empty
Solution:
  - Confirm there are active user sessions on the server
  - The application filters out technical sessions (console, services, listen)
  - Try refreshing the list with F5

Problem: Application won't start
Solution:
  - Check if Python is installed (if running from source)
  - Verify all required files are present
  - Run as Administrator if permission errors occur


KEYBOARD SHORTCUTS
------------------
F5           - Refresh session list
Enter        - Connect to selected session
Delete       - Logoff selected session
Escape       - Deselect current session
Double-Click - Quick connect to session
Right-Click  - Open context menu


SECURITY NOTES
--------------
• The application does not store any passwords or credentials
• All connections use Windows integrated authentication
• Session termination requires user confirmation
• Server list is stored locally in plain text
• No data is sent to external servers


TECHNICAL DETAILS
-----------------
• Built with: Python, Tkinter
• Session queries use: Windows "query session" command
• Connections use: Windows "mstsc" (Remote Desktop Client)
• Session termination: Windows "logoff" command
• Works with both English and Russian Windows versions
• Automatic detection of session states regardless of OS language


SUPPORT & DONATIONS
-------------------
Developer: Aleksey Pokrovskiy
Email:     a.pokrovskiy@live.com

If you find this tool useful, consider supporting its development.


KNOWN LIMITATIONS
-----------------
• Requires Windows OS (client and servers)
• Shadow connections may require specific Group Policy settings
• Some corporate firewalls may block session queries
• Maximum tested: 200+ concurrent sessions per server


VERSION HISTORY
---------------
v4.0 (Current)
  - Added bilingual support (English/Russian)
  - Implemented server management dialog
  - Added auto-refresh mode
  - Improved UI with modern design
  - Added keyboard shortcuts
  - Multi-threaded session loading
  - Real-time search filtering
  - About window with donation support


LICENSE
-------
© 2025 All rights reserved

This software is provided "as is" without warranty of any kind, express or
implied. Use at your own risk. The author is not responsible for any data
loss, system damage, or other issues arising from the use of this software.



              For updates and more information, contact:
                      a.pokrovskiy@live.com

