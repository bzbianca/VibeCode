**Deployment Document: Click and Drag Game with Rare Items**

**Version:** 1.0
**Date:** 2025-04-07
**Prepared By:** Gemini AI Assistant (Based on User-Provided Code)

**1. Introduction**

* **1.1 Purpose:** This document outlines the steps required to deploy the "Click and Drag Game with Rare Items" web application in a web server environment and provides instructions on how to run the game.
* **1.2 Audience:** This document is intended for web developers or system administrators responsible for hosting static HTML, CSS, and JavaScript web applications, as well as end-users who will play the game.
* **1.3 Scope:** This document covers the deployment of the HTML file (`index.html`) and the associated `items` folder containing image assets. It assumes the target environment has a web server capable of serving static content. It also details how to interact with the game in a web browser.
* **1.4 Assumptions:** The following assumptions are made prior to the deployment:
    * A web server (e.g., Apache, Nginx, a simple HTTP server) is already installed and configured on the target environment.
    * The user has the necessary permissions to upload files to the web server's document root or a designated directory.
    * The `items` folder contains the following image files: `basketballhoop.png`, `croissant.png`, `watermelon.png`, `mrgardner.png`, and `basketball.png`.
    * End-users have a modern web browser installed on their devices.

**2. Deployment Environment**

* **2.1 Target Environment:** [Specify the target environment - e.g., Production Web Server, Staging Web Server, Local Development Server]
* **2.2 Infrastructure:**
    * **Server:** [Specify server details if known - e.g., Hostname/IP Address, Operating System]
    * **Web Server:** [Specify the web server software - e.g., Apache HTTP Server, Nginx, Node.js `http-server`, Python `SimpleHTTPServer`]
    * **File System:** Access to the web server's file system to upload files.

**3. Deployment Prerequisites**

* **3.1 Software Requirements:** A web browser (Chrome, Firefox, Safari, Edge, etc.) is required to access and play the game. No specific server-side software beyond a web server is strictly necessary for this static application.
* **3.2 Configuration Files:** The primary configuration is within the `index.html` file itself (styling and JavaScript logic). No external configuration files are needed for basic deployment.
* **3.3 Build Artifacts:** The following files and folders are the build artifacts for deployment:
    * `index.html` (the main HTML file containing the game code)
    * `items/` (a folder containing the game's image assets)
        * `basketball.png`
        * `basketballhoop.png`
        * `croissant.png`
        * `mrgardner.png`
        * `watermelon.png`
* **3.4 Access Permissions:** Write access to the web server's document root or the designated deployment directory is required for deployment. Read access is required for the web server to serve the files to users.

**4. Deployment Steps**

* **4.1 Pre-Deployment Checklist:**
    * [ ] Ensure all image files are present in the `items` folder: `basketball.png`, `basketballhoop.png`, `croissant.png`, `mrgardner.png`, `watermelon.png`.
    * [ ] Verify the `index.html` file is in the root directory of the deployment package.
    * [ ] Confirm you have the necessary credentials and access method (e.g., FTP, SFTP, SSH) to upload files to your web server.
    * [ ] Identify the correct directory on your web server where website files are served from (this is often called the document root, public_html, or www).

* **4.2 Deployment Procedure:**

    * **Step 1: Access Your Web Server:**
        * **Using FTP (File Transfer Protocol):**
            1. Open your FTP client (e.g., FileZilla, Cyberduck).
            2. Enter your web server's hostname (or IP address), your FTP username, and your FTP password.
            3. Connect to the server.
            4. Navigate to the web server's document root or the specific directory where you want to host the game.
        * **Using SFTP (Secure File Transfer Protocol):**
            1. Open your SFTP client (e.g., FileZilla, Cyberduck).
            2. Enter your web server's hostname (or IP address), your SFTP username, and your SFTP password (or use an SSH key if configured).
            3. Connect to the server.
            4. Navigate to the web server's document root or the specific directory where you want to host the game.
        * **Using SSH (Secure Shell) and Command Line:**
            1. Open your terminal or command prompt.
            2. Connect to your server using SSH: `ssh your_username@your_server_ip` (replace with your credentials).
            3. Navigate to the desired directory on the server using `cd` (change directory) command. For example: `cd /var/www/html/`.
        * **Using a Hosting Control Panel (e.g., cPanel, Plesk):**
            1. Log in to your hosting control panel.
            2. Look for a "File Manager" or similar tool.
            3. Navigate to the directory where you want to upload the files.

    * **Step 2: Upload the `index.html` File:**
        * **FTP/SFTP/File Manager:** Locate the `index.html` file on your local computer and upload it to the chosen directory on the web server. Ensure it's at the top level of that directory.
        * **SSH:** You can use the `scp` command to securely copy the file: `scp /path/to/your/local/index.html your_username@your_server_ip:/path/on/server/` (replace the paths and credentials).

    * **Step 3: Upload the `items` Folder:**
        * **FTP/SFTP/File Manager:** Locate the `items` folder on your local computer and upload the entire folder to the same directory on the web server where you uploaded `index.html`. Make sure the folder structure is maintained (i.e., the `items` folder is directly alongside `index.html`).
        * **SSH:** You can use the `scp` command with the `-r` flag for recursive copy: `scp -r /path/to/your/local/items/ your_username@your_server_ip:/path/on/server/` (replace the paths and credentials).

    * **Step 4: Verify File Structure on the Server:**
        Using your FTP/SFTP client, File Manager, or SSH, confirm that the files and folder are in the correct location:
        ```
        [your_web_server_root]/
        ├── index.html
        └── items/
            ├── basketball.png
            ├── basketballhoop.png
            ├── croissant.png
            ├── mrgardner.png
            └── watermelon.png
        ```

    * **Step 5: Access the Game in Your Browser:**
        Open a web browser and go to the URL of your website followed by the path to the `index.html` file.
        * If `index.html` is in the root: `http://yourdomain.com/` or `http://your_server_ip/`
        * If you uploaded it to a subdirectory (e.g., `/games/`): `http://yourdomain.com/games/` or `http://your_server_ip/games/`

* **4.3 Post-Deployment Checks and Running the Game:**

    * **Verification of Deployment:**
        * [ ] Verify that the game loads correctly in the web browser without any console errors.
        * [ ] Check that all images (basketball, hoop, croissant, watermelon, Mr. Gardner) are loading as expected.
        * [ ] Ensure the "Rare Items Key" is displayed correctly in the top right corner.

    * **Running the Game:**
        1.  **Open a Web Browser:** Use a modern web browser such as Chrome, Firefox, Safari, or Edge.
        2.  **Navigate to the Game's URL:** In the browser's address bar, type in the web address (URL) where you deployed the `index.html` file. This will be the URL of your website, potentially followed by a subdirectory if you didn't deploy it to the root.
            * **Example (Root Deployment):** `http://yourdomain.com/` or `http://your_server_ip/`
            * **Example (Subdirectory Deployment):** `http://yourdomain.com/games/` or `http://your_server_ip/games/`
        3.  **Interact with the Items:** Once the page loads, you should see the basketball items and the basketball hoop at the top.
        4.  **Click and Drag:** Click on one of the basketball items with your mouse. While holding the mouse button down, drag the item across the screen.
        5.  **Release to Launch:** Release the mouse button to let go of the item. It will then be affected by gravity and the physics simulation.
        6.  **Score Points:** Try to drag and launch the basketball items into the basketball hoop at the top of the screen.
        7.  **Observe Scoring:** The score, displayed prominently in the center of the screen (initially "0"), will increase by one for each item that successfully passes through the hoop.
        8.  **Rare Item Spawning:** After every 5 successful scores, there's a chance a rare item (croissant, watermelon, or Mr. Gardner) will spawn on the left side of the screen. These items behave the same way as the regular basketballs – click and drag to launch them.
        9.  **Winning the Game:** The game has a specific win condition: if you successfully get the "Rare Item 3" (the image of Mr. Gardner) through the basketball hoop, an alert box will appear with the message "You Win!".
        10. **Continue Playing:** After winning (or without winning), you can continue to click, drag, and launch the items. The game will continue to spawn new items after every 5 points (with the chance of being a rare item).

    * **Testing Game Mechanics:**
        * [ ] Test the click and drag functionality of the items.
        * [ ] Confirm that the score updates correctly when items enter the goal.
        * [ ] Trigger the spawning of rare items (by reaching scores of 5, 10, 15, etc.) and verify their appearance.
        * [ ] Test if the "You Win!" alert appears when "Rare Item 3" (Mr. Gardner) goes through the hoop.

**5. Rollback Plan (in case of deployment failure)**

* **5.1 Rollback Strategy:** The primary rollback strategy for this static web application is to revert to the previous version of the `index.html` file and the `items` folder.
* **5.2 Rollback Steps:**
    * **Step 1:** If you made a backup before deployment, restore the previous `index.html` file and the previous state of the `items` folder to the web server.
    * **Step 2:** If no backup was made, you would need to redeploy the last known working version of the files. This emphasizes the importance of backups before any deployment.
    * **Step 3:** Clear the browser cache of users who might have accessed the broken version to ensure they load the correct, rolled-back version.

**6. Communication Plan**

* **6.1 Communication Channels:** bzbaccay@my.waketech.edu
* **6.2 Key Contacts:** Bianca Baccay

**7. Security Considerations**

* As this is a client-side game with no server-side processing, direct security vulnerabilities related to the application code are minimal. However, consider standard web server security practices:
    * Ensure the web server itself is properly configured and secured.
    * Use HTTPS to encrypt traffic between the user's browser and the server.
    * Be mindful of file permissions on the web server.