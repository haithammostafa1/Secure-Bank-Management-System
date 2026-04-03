# Bank Management System with User Permissions (C++) 🏦🔐

This is an advanced version of the Bank Management System, featuring a robust **User Authentication** and **Access Control** system. Each user has specific permissions that determine which parts of the system they can access, making it a secure and realistic console application.

## 🌟 New Advanced Features
- **Login Screen**: Secure access requiring a username and password.
- **Permissions System**: Uses `Bitwise` logic to grant/deny access to specific menus (e.g., only admins can manage users).
- **User Management**: A dedicated menu to Add, Delete, Update, and Find system users.
- **Enhanced Security**: Prevents deletion of the "Admin" user to ensure the system remains manageable.
- **Logout**: Seamlessly switch between users without restarting the application.

## 🛠️ Technical Deep Dive
- **Bitwise Permissions**: Permissions are stored as integers and checked using the `&` operator (e.g., `Permission & CurrentUser.Permissions == Permission`).
- **Data Architectures**: 
  - `stUser`: Manages administrative credentials and access levels.
  - `stClient`: Manages banking customer data.
- **Multi-File Storage**: 
  - `Clients.txt`: Stores financial records.
  - `Users.txt`: Stores administrative credentials.
- **Input Buffer Handling**: Uses `std::ws` to ensure clean string inputs during multi-step forms.

## 📋 Permissions Map
| Permission | Value |
| :--- | :--- |
| Full Access | -1 |
| Show Clients | 1 |
| Add Client | 2 |
| Delete Client | 4 |
| Update Client | 8 |
| Find Client | 16 |
| Transactions | 32 |
| Manage Users | 64 |

