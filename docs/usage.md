| [Home](../README.md) |
|----------------------|

# Usage
First, refer to the installation and [setup guide](setup.md) to get started. Use the example(s) found below to decide what provisioning options are avaialble out of the box.

## Utility Playbook &mdash; Clone FortiSOAR Module
This playbook gives you the ability to clone a FortiSOAR module. Currently there is no UI function to clone a module so this playbook was created to solve that need.
To use this playbook

1. Navigate to **Playbooks** -> **08 - SOC Utilities** collection
![Collection](./res/Collection.png)

2. Click the  **Clone FortiSOAR Module** playbook to open it
3. Click the play button at the top right

![Play Button](./res/play_button.png)

4. Click **Trigger Playbook** button at the bottom left

![Trigger Playbook](./res/trigger_playbook.png)

5. From the pop up box, select the module you want to clone from, and provide the name of what the new module should be called. For this example we are selecting **Alerts** as the "Old Module", and the name **Security Alerts** as the New Module

![Module Questions](./res/module_input_questions.png)

6. Click the **Next** button
7. This may take 10-15 seconds to run. After you will see a popup with two options.

![Playbook complete](./res/playbook_complete_dialog.png)

 - Option 1: If you are ready to publish the changed click the **Publish** button
 - Option 2: click the **Manual Review** button. you will need to manually publish by navigating the Modules section in the System Settings

1. The publish will take 1-2 minutes.

![Publish Message](./res/publish_message.png)

9.  Navigate to System Settings by clicking the Gear icon at the top right

![Publish Message](./res/system_settings.png)

10.   Click the **Roles** section from the left navigation pane.

![Roles](./res/roles.png)

11.   Click the **Full App Permissions** Role, or whichever role you want to assign the permissions for the new module
12.   Scroll until you find the new module name (Security Alerts in this example), and check all of the permission boxes as necessary.

![Module Permissions Message](./res/module_permissions.png)
13.   Click **Save** at the bottom left

> **Note**
> Repeat steps 12 and 13 for adding permissions on other roles if needed

> **Caution**
> If you need playbooks to create records in this module, make sure the playbook appliance has the CRUD permissions neccesary to access the module
14.   Navigate to the Navigation section of the settings

![Navigiation](./res/navigation.png)

15.  Find the new module in the Modules box and check the box.

![Alt text](./res/modules_box.png)

16. Click **Add to Menu**
17. Scroll to the very bottom of the page. You can then optionally change the icon of the module using the pencil icon to the right of the row.

![Module Row](./res/module_row.png)

18.  (Optional) Drag the row to where you want to the module displayed
19.  Click **Save** at the bottom left.
20.  Refresh the page using F5 on the keyboard, or the refresh button on the browser.

The new module is now visible in the navigation pane.

![Alt text](./res/navigation_icon.png)

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Contents](./contents.md) |
|-----------------------------------------|-------------------------------------------|---------------------------|
