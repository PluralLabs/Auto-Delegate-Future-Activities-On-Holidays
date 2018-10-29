# Delegate Future Workflow Tasks 
Adds an user interface to auto delegate future activities assigned to the user. 

![auto-delegate future activities](https://user-images.githubusercontent.com/37924741/47353729-97098c00-d6da-11e8-8f57-1910d0ac1cc9.gif)

#### **How it works:**

Auto-Delegate Future Workflow Tasks on Holidays which allows the user to Auto-Delegate their workflow activities to another user before going for a holiday vacation.

#### **Project Details:**

 Built Using: Aras 11.0 SP12

#### **Browsers Tested:**  
Google Chrome 69

#### **Installation:**

**Important!** Always back up your code tree and database before applying an import package or code tree patch!


#### **Pre-requisites:**

 1. Aras Innovator installed (version 11.0 SP12)
 2. Auto Delegate Future Workflow Tasks Package
 3. Before importing package delete **Form** of User Itemtype using root/innovator Login
 4. While importing login with root/innovator into importing tool.
 5. After importing package add **Form** of User Itemtype using root/innovator Login

#### **Installation Steps:**

 1. Backup your database and store the BAK file in a safe place.
 2. Open up the Aras Package Import tool.
 3. Enter your login credentials and click Login
**Note: You must login as root for the package import to succeed!**
4. Enter the package name in the TargetRelease field.
Optional: Enter a description in the Description field.
5. Enter the path to your local ..\ Auto-Delegate Future Activities\imports.mf file in the Manifest File field.
6. Select Auto-Delegate Future Activities in the Available for Import field.
7. Select Type = Merge and Mode = Thorough Mode.
8. Click Import in the top left corner.
9. Close the Aras Package Import tool.

#### **Usage:**

1. Log in to Aras.
2. Navigate to User Itemtype in TOC Pane
3. Select User > Go to Action > Delegate Future Workflow Tasks >
4. You will get the Global Config Form. Set Delegation Status as **ON** and select the user to whom you want to assign the workflow activities when the current logged in user is going for a leave in **Auto Assign to the**
5. Then view logged in User Item and check the Set Delegation Status as **ON** and **auto assign to** will be the new user.
6. On a Workflow Map Activity if the assigned users delegation status is On then the user of current activity gets delegated to newly auto assigned user.
7. By Default, variable named **em_groupIdentity_variable** is set as **False**. So that, this functionality works for Identity Alias(Individual Users)
8. In the case of group Identity, if the group identity contains the user whose delegation status is ON, value of variable **em_groupIdentity_variable** can be set to **True** then new group identity will be created with the Delegated User in it.


#### **Contributing**

1.	Fork it!
2.	Create your feature branch: git checkout -b my-new-feature
3.	Commit your changes: git commit -am 'Add some feature'
4.	Push to the branch: git push origin my-new-feature
5.	Submit a pull request
For more information on contributing to this project, another Plural Labs project, or any Plural Community project, shoot us an email at info@pluraltechnology.com.

#### **Credits**
Auto-Delegate Future Activities application created by Plural Aras Development Team.
