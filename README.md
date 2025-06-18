# 🧰 IT Helpdesk Ticketing Solutions – Project Summary

This documentation outlines four successfully resolved IT support tickets processed through the internal ticketing system that was provided by the Jira application which is free for a month of access. Each summary includes the issue reported, a high-level overview of the solution, and a link to detailed documentation.

## 🟢 Ticket 14:  Shared Drives

Summary:

User requested access to both a personal network drive and the department's Finance shared folder to store individual files and collaborate with colleagues

✅ Solution involved:

- Creating dedicated security groups in Active Directory for both Personal and Finance drive access.

- Assigning Bruce Wayne as a member of both groups.

- Setting up NTFS permissions on each shared folder to reflect group-based access control.

- Configuring the user's Active Directory profile to automatically map network drives on login:

  - Z: mapped to \\SERVER2022\Personal\bwayne

  - Finance drive mapped to \\SERVER2022\Finance --> on users PC


Final validation was done via remote access to confirm both drives appeared and were accessible on the user's device.

The ticket was documented and resolved via the Jira system with a closing note to the user.


View Ticket 14: 🔗 [ Go to Ticket 14 : Shared Drives](https://github.com/anthonydiazz/Helpdesk_Simulation)


## 🟢 Ticket 15: PDF Files Not Opening

Summary:
User couldn’t open PDF files as no appropriate program was installed.

✅ Solution involved:

- Remoting into the system (Desktop2).

- Identifying that PDFs were defaulting to Microsoft Edge.

- Installing Adobe Acrobat Reader.

- Setting Adobe as the default program for .pdf files.


View Ticket 15: 🔗 [ Go to Ticket 15 : PDF Files Not Opening](https://github.com/anthonydiazz/pdf_files_not_working)




## 🟢Ticket 16: Desktop Folder Redirection

Summary:

User asked for anything saved on their Desktop to automatically route to their personal network drive.

✅ Solution involved:

- Creating and linking a GPO for folder redirection.

- Setting redirection for the Desktop folder to \\SERVER2022\Personal\%username%\Desktop.

- Applying the policy to the proper OU (HR).

- Running gpupdate /force and resolving permission issues on the folder.

View Ticket 16: 🔗 [ Go to Ticket 16 : Desktop Folder Redirection](https://github.com/anthonydiazz/Redirect_Desktop)


## 🟢 Ticket 17: Recover Deleted Files

Summary:

User accidentally deleted a folder from their redirected Desktop.

✅ Solution involved:

- Verifying the deletion through the user’s folder on the file server.

- Enabling Shadow Copies on the server.

- Restoring a previous version of the Desktop folder using Previous Versions.

View Ticket 17: 🔗 [ Go to Ticket 17 : Recover Deleted Files](https://github.com/anthonydiazz/Deleted_files)






# ✅ Best Practices for IT Ticket Handling


When resolving user tickets, it’s essential to keep the following best practices in mind:

🗣️ 1. Greet and Prioritize the User

- Always begin by greeting the user and introducing yourself in the ticket comments.

- Be patient and understanding — users are often stressed when reaching out, and your calm, respectful tone can set the stage for smooth communication.


## 📢 2. Communicate with Supervisors Before Making Access Changes

- For tickets that involve shared drive access (e.g., ticket - 14) or changes to folder redirection policies (e.g., ticket - 16), always:

   - Confirm with the user’s department supervisor that access is authorized.

   - If you're changing broader policies (like Group Policy Objects), consult with your IT supervisor first to avoid unintended consequences for other users.



## 📝 3. Use Internal Notes Effectively


- Include PC names and context (e.g., user’s location or department) as internal notes — this was helpful throughout this project.

- Additionally, it’s good practice to include a brief note describing how the issue was resolved, which can be helpful when:

   - A similar issue arises in the future.

   - Someone else on the IT team needs to revisit the case.


## 🔄 4. Stay Calm 


- Even if the issue appears frustrating or unclear at first, remain calm and take a step-by-step approach.

- Validate every fix by testing from the user's perspective — either through remote login or having the user confirm.






















