# Lab: Explore Insider Risk Management in Microsoft 365

## Lab scenario
In this lab, you will walk through the process of setting up an insider risk policy, along with the basic prerequisites to configure and use insider risk management policies.  Note:  this lab will only provide visibility into what is required for setting up Insider risk management and options associated with creating a policy.  This lab does not include a task to trigger the policy, as the number of events that would need to occur to trigger a policy are outside of the scope of this exercise.


**Estimated Time**: 25-30 minutes

#### Task 1: In this task you, as the global administrator, will enable permissions for Insider Risk Management.  Specifically, you will add users to the Insider Risk Management role group to ensure that designated users can access and manage insider risk management features.  It may take up to 30 minutes for the role group permissions to apply to users across the organization. 

1.	Open Microsoft Edge. In the address bar enter **admin.microsoft.com**. Please open this in a new private window.

      ![](../Images/module4/lab12/main-1.png)

1. Sign in with your admin credentials.
    1. In the Sign in window, Get the user credentials provided in the environment details page and paste the value in the username section and then select **Next**.
     
        ![](../Images/module4/lab11/1-1.png)
     
        ![](../Images/module4/lab12/main-2.png)
    
    1. Enter the admin password which should be provided by your lab hosting provider. Select **Sign in**.
    
        ![](../Images/module4/lab12/main-3.png)
     
    1. When prompted to protect the account, Please select **Skip for now**.

        ![](../Images/module4/lab12/main-4.png)
     
    1. When prompted to stay signed- in, select **Yes**. This takes you to the Microsoft 365 admin center page.

1. From the left navigation pane of the Microsoft 365 admin center, select **Show all**.

    ![](../Images/module4/lab14/new1.png)

1. Under Admin centers, select **Security**.  A new browser page opens to the welcome page of the Microsoft 365 Defender portal.

    ![](../Images/module4/lab14/new2.png)

1. From the left navigation pane of the Microsoft 365 Defender portal, select **Permissions & roles**.  You may need to scroll down to see this option.

1. From the Permissions & roles page, under **Email & collaboration roles** select **Roles**.

    ![](../Images/module4/lab14/new3.png)

1. In the search bar, enter **Insider risk** then select the search icon (magnifying glass).  Notice the five roles that show up.  Each of these has different access levels.  Select **Insider risk management**.

    ![](../Images/module4/lab14/new4.png)
    
    ![](../Images/module4/lab14/new5.png)

1. In the window that opens, next to where it says Members, select **Edit**. you may need to scroll to find it.

    ![](../Images/module4/lab14/new6.png)

1. To add members to this role group, select **Choose members**.

    ![](../Images/module4/lab14/new7.png)

1. Select **+ Add** from the top of the page.

    ![](../Images/module4/lab14/new8.png)

1. From the list of names, select **MOD Administrator**, **Megan Bowen** and your account ie. name with **ODL_User uniqueID** then select **Add** at the bottom of the page, then select **Done** at the bottom of the page.

    ![](../Images/module4/lab14/new9.png)
    
    ![](../Images/module4/lab14/new10.png)

1. Verify the added members is correct then select **Save**.

    ![](../Images/module4/lab14/new11.png)

1. From the bottom of the Insider Risk Management window, select **Close**.

    ![](../Images/module4/lab14/new12.png)

1. Close all the tabs except the **admin.microsoft.com** and then sign out from the admin center page and sign-in back again to reflect the permissions added for users faster.

#### Task 2 (SKIP if you did the setup lab task to enable the audit log): Insider risk management uses Microsoft 365 audit logs for user insights and activities identified in policies and analytics insights. In this task, you will enable the Audit log search capability. Note:  It may take several hours after you turn on audit log search before you can return results when you search the audit log.  Although it can take several hours before you can search the audit log, it will not impact the ability to complete other tasks in this lab.

1. Select the browser tab labeled, **Microsoft 365 admin center - Home**.  If you previously closed this browser tab, open Microsoft Edge and in the address bar enter **admin.microsoft.com** and sign in with your admin credentials.

1. Under Admin centers, select **Compliance**.  A new browser page opens to the welcome page of the Microsoft 365 compliance center.  

1. From the left navigation panel of the Microsoft 365 compliance center, select **Show all**.

1. In the left navigation panel, under solutions, select **Audit**.

1. Verify that the **Search** tab is selected (underlined).

1. Once you land on the Audit page, wait 2-3 minutes.  If Auditing is NOT enabled, you will see a blue bar on the top of the page that says start recording user and admin activity.  Select **Start recording user and admin activity**.  Once auditing is enabled, the blue bar disappears.  If the blue bar is not present then auditing is already enabled, and no further action is required.

      ![](../Images/97.png)

1. Return to the home page of the Microsoft 365 compliance center by selecting **Home** from the left navigation panel.

1. Keep this browser tab open, as you will use it in the next task.

#### Task 3: In this task you will walk through the settings associated with the Insider Risk Management solution.  Insider risk management settings apply to all insider risk management policies, regardless of the template you choose when creating a policy. 

1. You should be on the Microsoft 365 compliance center home page. If not, Open the browser tab **Home - Microsoft 365 compliance**.

1. From the left navigation panel under Solutions, select **Insider risk management**.

    ![](../Images/module4/lab14/new13.png)

1. Before getting started with setting up a policy, there are some settings that need to be configured.  From the Insider Risk Management page, select the **setting cog icon** on the top-right corner of the page to access Insider Risk settings.  
    1. Privacy tab:  for users who perform activities matching your insider risk policies, this setting will determine whether to show their actual names or use anonymized versions to mask their identities.  Select **Do not show anonymized versions of usernames** then select **Save**.  Select the  **Policy indicators** tab.

          ![](../Images/module4/lab14/new14.png)
    
    1. Policy indicators tab: Once a policy triggering event occurs, activities that map to the selected indicators are used in determining the risk score, for the user. Policy indicators selected here are included the Insider risk policy templates.  Scroll to view all the indicators available and any associated information. Under **Office indicators**, select **Select all**, scroll down and then select **Save**.  Select the **Policy timeframes** tab.

          ![](../Images/module4/lab14/new15.png)
    1. Policy timeframes tab:  The timeframes you choose here go into effect for a user when they trigger a match for an insider risk policy.   The Activation window determines how long policies will actively detect activity for users and is triggered when a user performs the first activity matching a policy. Past activity detection Determines how far back a policy should go to detect user activity and is triggered when a user performs the first activity matching a policy.  Leave the default values.  Select the **Intelligent detections** tab.

          ![](../Images/module4/lab14/new16.png)
    1. Intelligent detections tab:  Review the options here.  Note the domains settings and how they relate to the indicators.

          ![](../Images/module4/lab14/new17.png)
    3. Other items listed in the settings are in preview.  Explore these at will and note that as a preview, they are subject to change.

1. To return to the Insider risk management overview, select **Insider risk management** from the top-left corner of the page, above where it says Settings.

    ![](../Images/module4/lab14/new18.png)

1. Keep this browser tab open, as you will use it in the next task.

#### Task 4:  In this task you will walk through the creation of a policy.

1. You should be on the Insider risk management page.  If not already there, open the browser tab labeled, **Insider risk management - Microsoft 365 compliance**.

1. From the Insider risk management overview page, select the **Policies** tab then select **+ Create**.  Configure each of the following policy tabs.

    ![](../Images/module4/lab14/new19.png)

    1. Policy template:  From the list of categories, select **Data leaks** then select **General data leaks**.  Note that templates within categories may have additional prerequisites.  Read the details associated with this template, then select **Next**.

         ![](../Images/module4/lab14/new20.png)
    
    1. Name and description:  enter a name, **SC900-InsiderRiskPolicy**, then select **Next**.

         ![](../Images/module4/lab14/new21.png)
    1. Users and groups:  Review the information box.  Leave the default setting, **Include all users and groups**.  Select **Next**.

         ![](../Images/module4/lab14/new22.png)
    1. Content to prioritize: Read the description. Select **I want to specify SharePoint sites, sensitivity labels, and/or sensitive info types as priority content**, then select **Next**.
         ![](../Images/module4/lab14/new23.png)
         
        1. SharePoint site: For this policy example, leave this blank, select **Next**
        1. Sensitive info types: for this policy example, leave this blank then select **Next**. 
        1. Sensitivity labels: for this policy example, leave this blank then select **Next**.

         ![](../Images/module4/lab14/new24.png)
         ![](../Images/module4/lab14/new25.png)
         ![](../Images/module4/lab14/new26.png)
    1. Indicators and triggering event: Review the detailed information.  The policy is triggered by either the user performing an exfiltration activity as as defined (select the information icons for each bullet point for more detailed information) OR a match to an existing Data Loss Prevention (DLP) policy.  Since you don’t have any DLP policy configured as part of this exercise, select **User performs an exfiltration activity**.  Scroll down to see what is automatically selected.  Note that the policy indicators you enabled in the previous task are checked.   Recall that these indicators will only be activated once the policy is triggered and any activities that map to these indicators  will be used in calculating a risk score for the user.  In addition, Sequence detection is enabled.  If a sequence of activities, as defined, is detected then it suggests greater risk.  Select the information icon for detailed information on which indicators are required.  This selection requires that certain indicators be selected and that devices be onboarded. Scroll down and Leave the defaults and click **Next**

         ![](../Images/module4/lab14/new27.png)
        
    1. Indicator Thresholds:  here you can specify default or custom thresholds associated with the indicators.  Recall the indicators are activated only after the policy trigger occurs so these thresholds do not influence when the policy is triggered. Select **Specify custom thresholds**, By selecting this option, you can see the current default values. Leave the defaults and select **Next**.

         ![](../Images/module4/lab14/new28.png)
    1. Finish:  review the settings, select **Submit**, then select **Done**.

1. You are back on the Policies tab of the Insider risk management page.  The policy you just created will be listed.  

1. In the policy you just created, the "Users in scope" field represents users that are currently being assigned risk scores by the policy.  Assigning users a risk scores occurs when the policy is triggered which is why the value shows 0.  An admin can configure a policy to start assigning risk scores to specific users, based on activity detected by the policies you selected, AND which bypasses the requirement that a triggering event is detected first.  To do this, select the empty circle next to the policy name to select the policy, then select **Start scoring activity for users**, which is shown above the policy table.  Populate each field, then select **Start scoring activity**.  It can take 24 hours for the users to appear on the 'Users' tab. After that time, you can select the users from that tab to review detected activities.

    ![](../Images/module4/lab14/new29.png)

#### Review
In this lab, you walked through the process of setting up an insider risk policy, along with the basic prerequisites to configure and use insider risk management policies.
