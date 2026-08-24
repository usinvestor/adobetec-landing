# 🔧 Troubleshooting Guide
## WordPress Divi + GoHighLevel Integration Issues

---

## ❓ Common Issues & Solutions

### **Issue #1: Form Not Appearing on Page**

**Symptoms:**
- Embed code pasted but form not visible
- Page loads but form area is blank

**Solutions:**
1. Check if code module is using "Code" or "Custom HTML"
2. Verify embed code is complete (starts with `<iframe`)
3. Clear browser cache (Ctrl+Shift+Delete)
4. Check if security plugin is blocking iframe
5. Try in incognito mode
6. Switch to Divi's "Custom HTML" module instead of "Code"

**Prevention:**
- Always test in new browser tab
- Use consistent module type
- Add CSS to make form container responsive

---

### **Issue #2: Leads Not Showing in GoHighLevel**

**Symptoms:**
- Form submitted but no lead in CRM
- Leads appear then disappear
- Wrong contact info captured

**Solutions:**
1. Verify form submission succeeded (look for confirmation message)
2. Check email address format (must be valid)
3. Verify GoHighLevel account is active
4. Check if form is properly published in GoHighLevel
5. Look in "Trash" folder if missing
6. Check for duplicate filters
7. Wait 5 minutes (slight delay possible)

**Prevention:**
- Test form before client launch
- Check lead notification settings
- Verify all required fields are marked
- Test with multiple submissions

---

### **Issue #3: Zapier Not Connecting WPForms to GoHighLevel**

**Symptoms:**
- Zap shows "off" or "error"
- Forms submit but no leads appear
- Zap created but not triggering

**Solutions:**
1. Verify WPForms plugin is active in WordPress
2. Check Zapier account has valid payment method
3. Reconnect WordPress auth in Zapier
4. Re-authenticate GoHighLevel connection
5. Test trigger step in Zapier
6. Check field mapping (verify all fields mapped)
7. Try "Retest trigger" in Zapier
8. Submit new form entry to trigger Zap

**Prevention:**
- Test Zap immediately after creation
- Keep API credentials updated
- Monitor Zap activity in Zapier dashboard
- Set up Zap notifications for failures

---

### **Issue #4: Email Automation Not Sending**

**Symptoms:**
- Leads submit form but no email received
- Email goes to spam
- Automation shows "off"

**Solutions:**
1. Verify automation is turned "ON"
2. Check email address is valid
3. Verify sender email is authenticated
4. Look for email in spam folder
5. Check automation trigger settings
6. Verify email has been tested
7. Check sending limits (GoHighLevel has daily caps)
8. Add sender to contact's email whitelist

**Prevention:**
- Always test automation before launching
- Use branded sender email
- Add authentication (SPF, DKIM)
- Check daily sending limits
- Monitor email deliverability

---

### **Issue #5: Divi Form Styling Not Matching Site**

**Symptoms:**
- GoHighLevel form looks different from website
- Form doesn't match brand colors
- Form doesn't resize on mobile

**Solutions:**
1. Customize GoHighLevel form styling (colors, fonts)
2. Add CSS to container in Divi
3. Adjust form width in GoHighLevel settings
4. Use custom domain for form (looks more professional)
5. Hide certain fields if not needed
6. Test on mobile device

**Prevention:**
- Style form before embedding
- Match colors to website theme
- Test responsiveness early
- Preview on mobile during design

---

### **Issue #6: Too Many Leads/Spam Submissions**

**Symptoms:**
- Spam bots filling out form
- Junk leads in CRM
- Form being abused

**Solutions:**
1. Add CAPTCHA to GoHighLevel form
2. Add required fields (phone number, etc.)
3. Use conditional fields (show more for serious inquiries)
4. Add minimum text length requirement
5. Block known spam IP addresses
6. Use webhook validation
7. Create filter/tag to mark spam

**Prevention:**
- Enable CAPTCHA from start
- Add qualifying questions
- Use email verification
- Review first submissions closely

---

### **Issue #7: WordPress Plugin Conflicts**

**Symptoms:**
- Page breaks after adding code module
- Form doesn't load in builder
- Divi builder crashes

**Solutions:**
1. Deactivate all plugins except Divi + essential
2. Reactivate one at a time to find culprit
3. Update all plugins to latest version
4. Check for plugin conflicts in WordPress admin
5. Clear site cache
6. Switch to default WordPress theme temporarily
7. Use browser dev tools (F12) to check console errors

**Prevention:**
- Keep plugins updated
- Use minimal, essential plugins
- Test in staging environment
- Monitor WordPress admin

---

### **Issue #8: GoHighLevel Automation Too Complex**

**Symptoms:**
- Can't figure out automation flow
- Leads not moving through pipeline
- Multiple automations conflicting

**Solutions:**
1. Start with single email automation
2. Map out flow before building (on paper/Figma)
3. Use simple triggers (form submission)
4. Add delays between emails (at least 1 day)
5. Test with single lead first
6. Check for conflicting automations
7. Use conditions sparingly
8. Document automation in text file

**Prevention:**
- Keep automations simple to start
- Document all automations
- Number emails (Email 1, Email 2, etc.)
- Review before launching
- Use templates for common sequences

---

### **Issue #9: Client Can't Log Into GoHighLevel**

**Symptoms:**
- Client says "password doesn't work"
- Can't access account
- Locked out of dashboard

**Solutions:**
1. Reset password for client
2. Create sub-account for client (recommended)
3. Verify email address is correct
4. Check if account is active
5. Try logging in as client to test
6. Check browser cookies/cache
7. Try different browser
8. Verify two-factor auth if enabled

**Prevention:**
- Create sub-account from start (not shared login)
- Send login credentials securely
- Enable password manager compatibility
- Create backup access method
- Document login process for client

---

### **Issue #10: Mobile Form Not Working**

**Symptoms:**
- Form works on desktop but not mobile
- Form fields cut off on phone
- Submit button unclickable

**Solutions:**
1. Test on actual mobile device (not just browser resize)
2. Adjust form width to 100% on mobile
3. Stack form fields vertically
4. Increase button size for touch
5. Reduce field label size
6. Use mobile-optimized theme
7. Test on different devices (iOS, Android)

**Prevention:**
- Always test on mobile first
- Use mobile-friendly form builder
- Preview in GoHighLevel mobile app
- Test with real mobile device
- Monitor mobile conversion rates

---

## 🚨 Emergency Fixes

### **Site Completely Broken?**
1. Deactivate Divi temporarily
2. Switch to default WordPress theme
3. Disable all plugins
4. Reactivate one by one
5. Identify culprit
6. Contact plugin support

### **All Leads Disappeared?**
1. Check "Trash" folder in GoHighLevel
2. Restore from backup if available
3. Check filters applied to contact list
4. Verify account is active
5. Contact GoHighLevel support

### **Can't Access Divi Builder?**
1. Clear browser cache
2. Try different browser
3. Disable browser extensions
4. Increase PHP memory limit in wp-config.php
5. Contact host support

---

## 📞 When to Ask for Help

**Contact GoHighLevel Support if:**
- Account locked/suspended
- Can't log in
- Data loss
- Email not sending (consistent issue)
- API problems

**Contact Divi Support if:**
- Builder not loading
- Module not working
- Design issues specific to Divi
- Performance problems

**Contact WordPress Host if:**
- Site completely down
- PHP errors
- Database issues
- Hacked site

---

## 🔍 Debugging Tools

**Browser Developer Tools (F12):**
- Right-click → Inspect Element
- Go to "Console" tab
- Look for red error messages
- Note any 404 or 403 errors

**WordPress Debug:**
Add to wp-config.php:
```php
define('WP_DEBUG', true);
define('WP_DEBUG_LOG', true);
define('WP_DEBUG_DISPLAY', false);
```

**GoHighLevel Status Page:**
- https://status.gohighlevel.com
- Check if service is down
- Look for scheduled maintenance

---

## 💡 Pro Troubleshooting Tips

✅ Always test in staging before production
✅ Take screenshots before making changes
✅ Clear cache between tests
✅ Use browser incognito mode
✅ Test with different email addresses
✅ Check browser console for errors
✅ Monitor email deliverability
✅ Keep GoHighLevel and WordPress updated
✅ Document all changes made
✅ Create backup before major updates

---

**Still stuck? Check GoHighLevel docs or contact support!**