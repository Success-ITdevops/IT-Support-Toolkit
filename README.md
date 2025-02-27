# IT-Support-Toolkit

## Table of Contents
1. [Description](#-description)
2. [Features](#-features)
3. [Installation](#-installation)
4. [Usage](#-usage)
5. [Password Policy Best Practices](#-password-policy-best-practices)
6. [Starter Scripts](#-starter-scripts)
7. [Running Tests](#-running-tests)
8. [Contributing](#-contributing)
9. [License](#-license)
10. [Show Your Support](#-show-your-support)

##  Description  
A collection of **scripts, tools, and guides** to help IT Support professionals automate common tasks, troubleshoot issues, and improve efficiency.

##  Features  
✅ Automated user account creation (Active Directory)  
✅ Password reset script  
✅ Network diagnostic tool  
✅ System health check scripts  
✅ IT documentation templates  
✅ Password policy enforcement (Active Directory)  
✅ System performance monitoring  

##  Installation  
### Prerequisites  
- Windows PowerShell (for AD-related scripts)  
- Python (for automation tasks)  
- Bash (for Linux-based tools)  

### Steps  
1. Clone the repository:  
   ```bash
   git clone https://github.com/Success-ITdevops/IT-Support-Toolkit.git
   ```  
2. Navigate to the project folder:  
   ```bash
   cd IT-Support-Toolkit
   ```  
3. Run the required script:  
   ```bash
   python network_diagnostic.py  # Example Python script
   ```  

##  Usage  
- **Active Directory User Creation**: Automate user account creation.  
- **Password Reset**: Quickly reset forgotten passwords.  
- **Network Diagnostic**: Run troubleshooting commands automatically.  
- **System Health Check**: Monitor performance metrics.  
- **Password Policy Enforcement**: Ensure compliance with security policies.  
- **System Performance Monitoring**: Check CPU, memory, and disk usage.  

## 🔒 Password Policy Best Practices  
The following **Active Directory password policy settings** are recommended for security:  
- ✅ **Enforce password history**: 24 passwords remembered  
- ✅ **Maximum password age**: 42 days  
- ✅ **Minimum password age**: 1 day  
- ✅ **Minimum password length**: 10 characters  
- ✅ **Password complexity**: Enabled  
- ✅ **Store passwords using reversible encryption**: Disabled
- ### **Example Password Policy Configuration**  
Below is a screenshot showing a **Group Policy Management Editor** configuration enforcing these password policies:
[img]https://i.imgur.com/jiyV6hD.jpeg[/img]
<img src="https://i.imgur.com/jiyV6hD.jpeg" height="80%" width="80%" alt="Active Directory Group Policy Mgt"/>
<br />
<br />

## 🧪 Starter Scripts  
### **Password Reset Script (PowerShell)**  
```powershell
# Reset a user's password in Active Directory
param (
    [string]$Username,
    [string]$NewPassword
)
Set-ADAccountPassword -Identity $Username -NewPassword (ConvertTo-SecureString -AsPlainText $NewPassword -Force) -Reset
Write-Host "Password for $Username has been reset."
```

### **Password Policy Compliance Script (PowerShell)**  
```powershell
# Check Active Directory password policies
Get-ADDefaultDomainPasswordPolicy | Format-List
```

### **Network Diagnostic Script (Python)**  
```python
import os

def network_diagnostic():
    print("Running network diagnostics...")
    os.system("ping 8.8.8.8")
    os.system("ipconfig /all")
    os.system("netstat -an")
    os.system("tracert 8.8.8.8")
    os.system("nslookup google.com")
    os.system("netsh advfirewall show allprofiles state")

if __name__ == "__main__":
    network_diagnostic()
```

## 🧪 Running Tests  
```bash
pytest  # For Python-based scripts
```
## 🤝 Contributing  
Contributions are welcome! Feel free to submit pull requests with improvements.  

## 🐝 License  
This project is licensed under the **MIT License** – see the `LICENSE` file for details.

## 🌟 Show Your Support  
If you find this toolkit useful, **⭐ star the repository** and share with fellow IT professionals!
