# SC-300 Lab 01: Manage User Roles

Hands-on lab from Microsoft's SC-300 (Identity and Access Administrator) course. It covers creating users in Microsoft Entra ID, assigning and removing directory roles, bulk user provisioning, deleting and restoring users, and assigning licenses.

**Lab source:** [SC-300 Identity and Access Administrator – Lab 01](https://microsoftlearning.github.io/SC-300-Identity-and-Access-Administrator/Instructions/Labs/Lab_01_ManageUserRoles.html)
---

## Scenario

A new employee is joining as an application administrator. Create the user, assign the right role, and verify the permissions.

---

## Exercise 1: Create a new user and test default rights

- Created user **Chris Green** (`ChrisG`) in Entra ID with an auto-generated password.
- Signed in with an InPrivate window, changed the password on first login.
- Confirmed that the new user could not create their own enterprise application. New accounts have no privileged access by default.

## Exercise 2: Assign the Application Administrator role

- Assigned the **Application Administrator** role to Chris Green as an active assignment with a justification.
- Signed in as Chris again and confirmed that **+ Create your own application** was now available.

**Key takeaway:** Directory roles grant scoped administrative rights. They don't grant full admin access.

## Exercise 3: Remove a role assignment

- Removed the Application Administrator role from Chris Green through **Microsoft Entra roles and administrators**, using the role's Assignments page as an alternative to the user's profile.

**Key takeaway:** Removing roles on a regular basis supports least-privilege governance.

## Exercise 4: Bulk user provisioning

- **CSV bulk create:** Edited the sample `SC300BulkUser.csv` (replaced the domain placeholder) and uploaded it through **Users > Bulk operations > Bulk create**.
- **PowerShell with Microsoft Graph:** Connected with `Connect-MgGraph -Scopes "User.ReadWrite.All"`, then created a user with `New-MgUser`.

**Key takeaway:** Bulk operations and scripting scale provisioning far beyond what the portal can handle by hand.

## Exercise 5: Delete and restore a user

- Deleted Chris Green from **All users**.
- Restored the account from **Deleted users > Restore user**.

**Key takeaway:** Deleted users stay in a soft-delete state for 30 days, so accidental deletions can be recovered.

## Exercise 6: Assign a Windows Enterprise E3 license

- Confirmed the target user (Raul Razo) had a usage location set and no license.
- Assigned a **Windows 10/11 Enterprise E3** license from the **Microsoft 365 admin center** (Billing > Licenses).
- Verified the assignment in Entra ID under the user's Licenses page.

**Key takeaway:** A usage location must be set before a license can be assigned, and license changes are made in the Microsoft 365 admin center.

---

## Screenshots

<!-- Add screenshots to a /screenshots folder and reference them here -->
- ![User created](screenshots/01-user-created.png)
- ![Application Administrator role assigned](# SC-300 Lab 01: Manage User Roles

Hands-on lab from Microsoft's SC-300 (Identity and Access Administrator) course. It covers creating users in Microsoft Entra ID, assigning and removing directory roles, bulk user provisioning, deleting and restoring users, and assigning licenses.

**Lab source:** [SC-300 Identity and Access Administrator – Lab 01](https://microsoftlearning.github.io/SC-300-Identity-and-Access-Administrator/Instructions/Labs/Lab_01_ManageUserRoles.html)

**Environment:** Microsoft 365 E5 tenant (trial), Microsoft Entra admin center, Microsoft 365 admin center, PowerShell 7.2+ with Microsoft Graph PowerShell

---

## Scenario

A new employee is joining as an application administrator. Create the user, assign the right role, and verify the permissions.

---

## Exercise 1: Create a new user and test default rights

- Created user **Chris Green** (`ChrisG`) in Entra ID with an auto-generated password.
- Signed in with an InPrivate window, changed the password on first login.
- Confirmed that the new user could not create their own enterprise application. New accounts have no privileged access by default.

## Exercise 2: Assign the Application Administrator role

- Assigned the **Application Administrator** role to Chris Green as an active assignment with a justification.
- Signed in as Chris again and confirmed that **+ Create your own application** was now available.

**Key takeaway:** Directory roles grant scoped administrative rights. They don't grant full admin access.

## Exercise 3: Remove a role assignment

- Removed the Application Administrator role from Chris Green through **Microsoft Entra roles and administrators**, using the role's Assignments page as an alternative to the user's profile.

**Key takeaway:** Removing roles on a regular basis supports least-privilege governance.

## Exercise 4: Bulk user provisioning

- **CSV bulk create:** Edited the sample `SC300BulkUser.csv` (replaced the domain placeholder) and uploaded it through **Users > Bulk operations > Bulk create**.
- **PowerShell with Microsoft Graph:** Connected with `Connect-MgGraph -Scopes "User.ReadWrite.All"`, then created a user with `New-MgUser`.

**Key takeaway:** Bulk operations and scripting scale provisioning far beyond what the portal can handle by hand.

## Exercise 5: Delete and restore a user

- Deleted Chris Green from **All users**.
- Restored the account from **Deleted users > Restore user**.

**Key takeaway:** Deleted users stay in a soft-delete state for 30 days, so accidental deletions can be recovered.

## Exercise 6: Assign a Windows Enterprise E3 license

- Confirmed the target user (Raul Razo) had a usage location set and no license.
- Assigned a **Windows 10/11 Enterprise E3** license from the **Microsoft 365 admin center** (Billing > Licenses).
- Verified the assignment in Entra ID under the user's Licenses page.

**Key takeaway:** A usage location must be set before a license can be assigned, and license changes are made in the Microsoft 365 admin center.

---

## Screenshots

<!-- Add screenshots to a /screenshots folder and reference them here -->
- ![User created](<img width="739" height="338" alt="image" src="https://github.com/user-attachments/assets/8606bd0c-c468-415c-a3d6-91ec93d15d51" />
)
- ![Application Administrator role assigned](<img width="766" height="251" alt="image" src="https://github.com/user-attachments/assets/d3edcf22-c1b6-4ae5-867c-c7d307be20db" />
)
- ![Role removed](<img width="578" height="265" alt="image" src="https://github.com/user-attachments/assets/01fd84e0-e98e-4add-9e0f-ea0bdf1a793f" />
)
- ![Bulk create](screenshots/04-bulk-create.png)
- ![User restored](<img width="753" height="234" alt="image" src="https://github.com/user-attachments/assets/49f3aa47-d59a-4b47-bc51-cac7b5b495f9" />
)
- ![License assigned](<img width="758" height="233" alt="image" src="https://github.com/user-attachments/assets/703753b5-4ba5-4c2d-a4aa-b67758e980e0" />
)
<img width="764" height="292" alt="image" src="https://github.com/user-attachments/assets/710fc016-7e8c-4516-a4ae-22f6bbdc7810" />

## Lessons learned

<!-- Add anything that tripped you up, e.g. PIM prompts, PowerShell version, CSV formatting -->

## Next steps

- Continue with the next SC-300 lab.
- Use the Microsoft Graph PowerShell commands from Exercise 4 to build out the RBAC auditing work.)
- ![Role removed](screenshots/03-role-removed.png)
- ![Bulk create](screenshots/04-bulk-create.png)
- ![User restored](screenshots/05-user-restored.png)
- ![License assigned](screenshots/06-license-assigned.png)

## Lessons learned

<!-- Add anything that tripped you up, e.g. PIM prompts, PowerShell version, CSV formatting -->

## Next steps

- Continue with the next SC-300 lab.
- Use the Microsoft Graph PowerShell commands from Exercise 4 to build out the RBAC auditing work.
