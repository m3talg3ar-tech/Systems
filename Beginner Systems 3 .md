

### Key Points

#### 1. **Learning Objectives:**
   - Understand basic user administration.
   - Learn how to elevate privileges appropriately (root).
   - Set permissions for folders/files correctly.
   - Manage extended permissions.

#### 2. **User Administration Commands:**
   - `adduser`: Adds a user and sets up the account, prompting for necessary values like password and home directory setup.
   - `useradd`: Creates a basic user account without prompting for additional details (less intuitive).
   - `deluser` or `userdel`: Deletes a user. The `-r` flag removes the associated home directory.

#### 3. **User Information:**
   - User information is stored in `/etc/passwd`.
   - Each line represents one user and contains seven fields separated by colons.
   - Root has UID (User ID) of `0`, which should not be duplicated for security reasons.

#### 4. **Group Administration Commands:**
   - `addgroup`: Adds a group.
   - `delgroup`: Deletes a group.
   - `groups <user>`: Shows the current user’s groups or shows `<user>’s` groups if specified.

#### 5. **User Modification Command:**
   - `usermod`: Modifies an existing user account, e.g., changing UID/GID, home directory, etc.

#### 6. **Permissions and Groups in Linux:**
   - Permissions are managed through the `/etc/group` file.
   - One group can have many users; one user can belong to multiple groups.

#### 7. **File Permission Basics:**
   - Three sets of permissions define access: owner, group owners, everyone else (world).
   - Each set has three bits for read (`r`), write (`w`), and execute (`x`) operations.
   - Permissions are represented using symbolic notation (`chmod +/-notation u,g,o,a` or numeric notation `754`).

#### 8. **Changing File Ownership:**
   - Use the `chown owner:group <file>` command to change file ownership.

#### 9. **Default Permission Settings (Umask):**
   - The default permission bits are set by umask.
   - A common umask value is `022`, which removes write permissions for group and others.

#### 10. **Changing File Permissions:**
    - Use the `chmod` command to change file permissions:
      - Symbolic notation: e.g., `chmod +x <file>`.
      - Numeric notation: e.g., `chmod 754 <file>`.

#### 11. **Switching Users with Root Privileges:**
    - Use the `su` command to switch users, often used for root access.

#### 12. **Privilege Elevation (sudo):**
   - Instead of multiple root accounts, use a program like sudo which allows controlled elevation of privileges.
   - This is more secure and avoids potential security holes associated with multiple UID 0 accounts.

#### 13. **Group ID (GID) Management:**
    - GID `0` is reserved for the group called "root" or "system".
    - It’s important to avoid assigning other groups a GID of `0`.

#### 14. **Permissions and Operations on Files:**
   - Nine permission bits determine which operations can be performed:
     - Read (`r`), write (`w`), execute (`x`) for owner, group, and others.

#### 15. **Useful Commands Summary:**
    - `adduser`: Adds a user with home directory setup.
    - `deluser` or `userdel`: Deletes users; `-r` flag removes the associated home directory.
    - `usermod`: Modifies existing user accounts.
    - `chmod`: Changes file permissions using symbolic (`u,g,o,a`) and numeric notations.
    - `chown`: Changes ownership of files.

These points cover essential aspects of managing users, groups, and permissions in a Linux environment as described in the document.
