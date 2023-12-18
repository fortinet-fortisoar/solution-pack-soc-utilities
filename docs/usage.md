| [Home](../README.md) |
|----------------------|

# Usage
First, refer to the installation and [setup guide](setup.md) to get started. Use the example(s) found below to decide what provisioning options are avaialble out of the box.

## Utility Playbook &mdash; Clone FortiSOAR Module
This playbook gives you the ability to clone a FortiSOAR module. Currently there is no UI function to clone a module so this playbook was created to solve that need.

## New Module Creation:

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

   >**Note:** If Module with same name already exists. A popup with error message appears.
      ![Error Message](./res/error_message.png)

7. This may take 10-15 seconds to run. After you will see a popup with two options.

   ![Playbook complete](./res/playbook_complete_dialog.png)

 - Option 1: If you are ready to publish the changed click the **Publish** button
 - Option 2: click the **Manual Review** button. you will need to manually publish by navigating the Modules section in the System Settings

8. The publish will take 1-2 minutes.

   ![Publish Message](./res/publish_message.png)

## Module Permission

1. Navigate to System Settings by clicking the Gear icon at the top right

   ![Publish Message](./res/system_settings.png)

2. Click the **Roles** section from the left navigation pane.

   ![Roles](./res/roles.png)

3. Click the **Full App Permissions** Role, or whichever role you want to assign the permissions for the new module

4. Scroll until you find the new module name (Security Alerts in this example), and check all of the permission boxes as necessary.

   ![Module Permissions Message](./res/module_permissions.png)

5. Click **Save** at the bottom left

> **Note:** Repeat steps 4 and 5 for adding permissions on other roles if needed

> **Caution:** If you need playbooks to create records in this module, make sure the playbook appliance has the CRUD
> permissions necessary to access the module

6. Navigate to the Navigation section of the settings

   ![Navigiation](./res/navigation.png)

7. Find the new module in the Modules box and check the box.

   ![Alt text](./res/modules_box.png)

8. Click **Add to Menu**

9. Scroll to the very bottom of the page. You can then optionally change the icon of the module using the pencil icon to
   the right of the row.

   ![Module Row](./res/module_row.png)

10. (Optional) Drag the row to where you want to the module displayed.

11. Click **Save** at the bottom left.
12. Refresh the page using F5 on the keyboard, or the refresh button on the browser.

   The new module is now visible in the navigation pane.

   ![Alt text](./res/navigation_icon.png)

## Utility Playbook &mdash; Terminates Pending Manual Inputs
This playbook gives you the ability to terminate all manual inputs that are pending for an user action/input created before the specified timestamp.

1. Navigate to Alerts module then click to the **Execute** Button

2. Select the **Terminates Pending Manual Inputs** playbook for trigger

   ![Terminate Manual Input](./res/trigger_terminate_manual_input.png)

3. Select the DateTime using which you want to terminate all manual inputs that have been created before the specified timestamp.

   ![TillDate](./res/till_date.png)
   
5. After successfully executing the playbook, terminates all manual inputs pending for an user action/input created before the specified timestamp.

   ![Result](./res/output_terminate_manual_input_playbooks.png)

## Utility Playbook &mdash; Terminate Awaiting Data Ingestion playbooks

This playbook gives you the ability to terminate a list of data ingestion playbooks which are in awaiting state till the specified last x minutes.

1. Navigate to Alerts module then click to the **Execute** Button

2. Select the **Terminate Awaiting Data Ingestion playbooks** playbook for trigger

   ![Terminate Data Ingestion Playbooks](./res/terminate_dl_playbooks.png)

3. Provide last x minutes, terminate list of data ingestion playbooks which are in awaiting state till the specified last x minutes.

   ![Terminate Data Ingestion Playbooks](./res/last_x_minute.png)
   
5. After successfully executing the playbook, terminate list of data ingestion playbooks which are in awaiting state till the specified last x minutes.

   ![Result](./res/output_terminate_dl_playbooks.png)

## Utility Playbook &mdash; Extract Related Alert of Pending Manual Input in CSV

This playbook gives you the ability to retrieves all pending manual input records for an user action/input and generates CSV.

1. Navigate to Alerts module then click to the **Execute** Button

2. Select the **Extract Related Alert of Pending Manual Input in CSV** playbook for trigger

   ![Play Button](./res/trigger_playbook_option.png)

3. After successfully executing the playbook, retrieves all pending manual input records for an user action/input and
   generates CSV and stores it as an attachment in FortiSOAR attachment module for related and missing alerts.
   
   ![Play Button](./res/csv_attachment.png)

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Contents](./contents.md) |
|-----------------------------------------|-------------------------------------------|---------------------------|



