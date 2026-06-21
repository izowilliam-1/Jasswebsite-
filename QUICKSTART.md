# 🎯 JASS Portal - Quick Start Guide

Welcome to your deployed JASS Portal! This guide will help you access all features.

---

## 📍 Main Access Points

### 🏠 Public Portal
**URL**: https://Izo-200812.github.io/Jass-portal/

This is your main landing page with:
- Portal overview
- Available applications
- Platform features
- Quick navigation to all tools

---

## 🔐 Admin Access Portal

### Admin Login
**URL**: https://Izo-200812.github.io/Jass-portal/admin-login.html

**Default Credentials:**
```
Username: admin
Staff Code: JASS2026
```

After login, you'll have access to all admin features.

---

## 📊 Admin Dashboard
**URL**: https://Izo-200812.github.io/Jass-portal/admin-dashboard.html
*(Accessible after admin login)*

### Features:
- 👥 Student Management
  - Add new students
  - View student list
  - Search and manage records
  
- 📈 Grade Management
  - Record grades by subject
  - View grade history
  - Calculate averages
  
- ✓ Attendance Tracking
  - Mark daily attendance
  - View attendance records
  - Generate reports
  
- 💰 Fee Management
  - Record fee payments
  - Track outstanding fees
  - View payment status

---

## 🔑 Security Center
**URL**: https://Izo-200812.github.io/Jass-portal/admin-password-manager.html
*(Accessible after admin login)*

### Features:
- 🔑 **Change Password**
  - Update staff code
  - Strong password requirements
  - Real-time strength indicator
  
- 📋 **Password History**
  - View all password changes
  - Track security updates
  
- 🔐 **Security Settings**
  - Enable 2FA (SMS, Email, Authenticator App)
  - Configure session timeout
  - Setup login alerts
  - Add IP whitelist
  
- 📱 **Session Management**
  - View active sessions
  - Logout from other devices
  - Emergency logout all sessions

---

## 👥 Access Control System
**URL**: https://Izo-200812.github.io/Jass-portal/admin-rbac.html
*(Accessible after admin login)*

### Features:
- 🎯 **Manage Roles**
  - 5 pre-defined system roles (locked)
  - Create custom roles
  - View role statistics
  - Assign permissions
  
- 🔐 **Manage Permissions**
  - 10 core permissions
  - Organized by categories
  - Assign to roles
  
- 👤 **User Access Control**
  - Assign roles to users
  - Set role status (Active/Inactive)
  - Track assignments
  
- 📊 **Role Matrix**
  - Complete role-permission overview
  - Export as CSV
  - Visual mapping

### Pre-defined Roles:
1. **Super Admin** - Full system access
2. **Registrar** - Student records & registration
3. **Teacher** - Grade & attendance management
4. **Finance Officer** - Fee & payment management
5. **Student** - Limited student access

---

## 📋 Audit Logging System
**URL**: https://Izo-200812.github.io/Jass-portal/admin-audit-logs.html
*(Accessible after admin login)*

### Features:
- 📊 **Dashboard**
  - Real-time statistics
  - Recent activity (7-day chart)
  - Action summary
  
- 📝 **Activity Logs**
  - View all system activities
  - Advanced filtering by:
    - Action type
    - Username
    - Date range
  - Detailed log inspection
  - Export to CSV
  
- 👤 **User Activity Tracking**
  - User activity summary
  - Action counts
  - Last activity tracking
  - Login counts
  
- ⚙️ **System Events**
  - Critical system events
  - Event monitoring
  - Status tracking
  
- 📈 **Reports**
  - Generate custom reports
  - Activity reports
  - Security reports
  - User activity reports
  - Compliance reports
  - Export reports

---

## 🔄 Workflow Example

### First Time Setup:
1. Navigate to: https://Izo-200812.github.io/Jass-portal/
2. Click on "Open App" for any section or navigate to `/admin-login.html`
3. Login with credentials: `admin` / `JASS2026`
4. Go to Security Center and change your password
5. Setup 2FA for extra security
6. Configure roles and permissions in Access Control
7. Assign roles to team members
8. Start managing students, grades, and fees
9. Monitor all activities in Audit Logs

---

## 💾 Data Storage

All data is stored in your browser's LocalStorage. This means:
- ✅ Data persists across browser sessions
- ❌ Data is device-specific (not synced across devices)
- ⚠️ Clearing cache will delete data
- 📝 For production, backend integration needed

### Important Files to Backup:
- All configurations in Access Control
- Password change history
- Audit logs
- User role assignments

---

## 🔒 Security Tips

1. **Change Default Credentials**
   - Go to Security Center
   - Update your staff code
   - Enable 2FA

2. **Regular Password Changes**
   - Change your staff code monthly
   - Use strong passwords (8+ chars, mixed case, numbers, symbols)
   - Track changes in password history

3. **Monitor Activities**
   - Regularly review audit logs
   - Check user activities
   - Monitor system events

4. **Session Management**
   - Logout when done
   - Monitor active sessions
   - Remove suspicious sessions

5. **Role Management**
   - Assign least privilege
   - Remove unused roles
   - Audit permission changes

---

## ⚠️ Important Notes

### Current Version (Frontend-Only):
- All data stored in browser LocalStorage
- No backend database
- Single device data storage
- Not suitable for multi-device sync

### For Production Use:
You should:
1. Implement a backend API (Node.js, Python, etc.)
2. Setup a database (MongoDB, PostgreSQL, etc.)
3. Add server-side authentication
4. Encrypt sensitive data
5. Use HTTPS/SSL
6. Setup regular backups

### Deployment:
- Automatic via GitHub Pages
- Changes deploy on push to main branch
- No build process required
- Can take 2-5 minutes to update

---

## 🚨 Troubleshooting

### Can't access admin panel?
1. Make sure you're using: `/admin-login.html`
2. Check credentials: `admin` / `JASS2026`
3. Clear browser cache and try again
4. Try incognito/private window

### Lost data?
1. Check if data is in browser LocalStorage
2. Open DevTools (F12) → Application → LocalStorage
3. Look for keys starting with `jass_`
4. If gone, data cannot be recovered (unless backed up)

### Slow performance?
1. Too many audit logs stored
2. Reduce log retention period
3. Export and archive old logs
4. Clear browser cache

### Session expired?
1. You're logged out after 1 hour inactivity
2. Login again to continue
3. Adjust timeout in Security Center if needed

---

## 📱 Responsive Design

All pages are mobile-responsive and work on:
- 📱 Mobile devices
- 📊 Tablets
- 🖥️ Desktop computers
- 🎮 Wide screens

---

## 🎓 Features by Role

### Super Admin
- ✅ Everything
- ✅ Manage users and roles
- ✅ Access all reports
- ✅ View audit logs

### Registrar
- ✅ Manage students
- ✅ View grades
- ✅ Track attendance
- ✅ Generate reports

### Teacher
- ✅ Record grades
- ✅ Mark attendance
- ✅ View reports
- ❌ Cannot manage students
- ❌ Cannot access fees

### Finance Officer
- ✅ Manage fees
- ✅ Record payments
- ✅ View financial reports
- ❌ Cannot modify grades

### Student
- ✅ View own grades
- ✅ View attendance
- ✅ View reports
- ❌ Limited access to system

---

## 📞 Support

### Self-Service:
1. Check DEPLOYMENT.md for detailed guide
2. Review inline code comments in HTML files
3. Check browser console for errors
4. Use browser DevTools for debugging

### Manual Activities:
- Export logs regularly
- Backup important data
- Document custom configurations
- Keep deployment guide updated

---

## 🎉 You're Ready!

Your JASS Portal is now deployed and ready to use!

**Start here:**
1. Go to: https://Izo-200812.github.io/Jass-portal/
2. Login to admin: `/admin-login.html`
3. Explore all features
4. Change default credentials
5. Configure for your organization

**For detailed information**, see DEPLOYMENT.md

---

**Deployed on**: 2026-06-11
**Last Updated**: 2026-06-11
**Version**: 1.0.0
