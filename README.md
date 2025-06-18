#🧰 IT Helpdesk Ticketing Solutions – Project Summary

This documentation outlines four successfully resolved IT support tickets processed through the internal ticketing system. Each summary includes the issue reported, a high-level overview of the solution, and a link to detailed documentation.

🟢 Ticket 14:  Shared Drives

Summary:

User requested access to two shared drives — one personal and one department-specific (Finance).

✅ Solution involved:

- Creating two Active Directory security groups (Personal and Finance).

- Adding the user to both groups.

- Assigning NTFS permissions.

- Mapping the drives via AD and verifying access remotely.



🟢 Ticket 15: PDF Files Not Opening

Summary:
User couldn’t open PDF files as no appropriate program was installed.

✅ Solution involved:

- Remoting into the system (Desktop2).

- Identifying that PDFs were defaulting to Microsoft Edge.

- Installing Adobe Acrobat Reader.

- Setting Adobe as the default program for .pdf files.


View Ticket 15: 🔗 [ Go to Ticket 15 : PDF Files Not Opening](https://github.com/anthonydiazz/pdf_files_not_working)




Ticket 16: Desktop Folder Redirection

Summary:

User asked for anything saved on their Desktop to automatically route to their personal network drive.

✅ Solution involved:

- Creating and linking a GPO for folder redirection.

- Setting redirection for the Desktop folder to \\SERVER2022\Personal\%username%\Desktop.

- Applying the policy to the proper OU (HR).

- Running gpupdate /force and resolving permission issues on the folder.


🟢 Ticket 17: Recover Deleted Files

Summary:

User accidentally deleted a folder from their redirected Desktop.

✅ Solution involved:

- Verifying the deletion through the user’s folder on the file server.

- Enabling Shadow Copies on the server.

- Restoring a previous version of the Desktop folder using Previous Versions.

