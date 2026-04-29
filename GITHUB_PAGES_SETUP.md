# Fin.India Holdings Landing Page - GitHub Pages Deployment Guide

## Step-by-Step Setup (5 minutes)

### **Step 1: Create a GitHub Repository**
1. Go to [github.com](https://github.com) and log in (create account if needed)
2. Click **"New"** (green button, top-left)
3. Enter Repository name: `fin-india-wedding` or `{your-username}.github.io`
   - **Option A:** Use `{your-username}.github.io` → Live at `https://{your-username}.github.io`
   - **Option B:** Use `fin-india-wedding` → Live at `https://{your-username}.github.io/fin-india-wedding`
4. Select **Public** (required for free GitHub Pages)
5. Click **Create repository**

---

### **Step 2: Upload the HTML File**

**Method A: GitHub Web Interface (Easiest)**
1. In your new repository, click **Add file** → **Upload files**
2. Drag & drop `fin-india-wedding-landing.html` into the upload area
3. Name it **`index.html`** (GitHub Pages looks for this file by default)
4. Scroll down and click **Commit changes**

**Method B: Using Git Command Line**
```bash
# Clone your repo
git clone https://github.com/YOUR-USERNAME/fin-india-wedding.git
cd fin-india-wedding

# Copy the HTML file
cp /path/to/fin-india-wedding-landing.html index.html

# Push to GitHub
git add index.html
git commit -m "Add Fin.India Holdings landing page"
git push origin main
```

---

### **Step 3: Enable GitHub Pages**

1. In your repository, go to **Settings** (top navigation)
2. Click **Pages** (left sidebar)
3. Under "Build and deployment":
   - Source: Select **Deploy from a branch**
   - Branch: Select **main** and **/ (root)**
4. Click **Save**

---

### **Step 4: Access Your Live Website**

Within 1-2 minutes, your site will be live at:

- **If using `{username}.github.io`:** 
  ```
  https://YOUR-USERNAME.github.io
  ```

- **If using `fin-india-wedding`:**
  ```
  https://YOUR-USERNAME.github.io/fin-india-wedding
  ```

GitHub will show the URL in the Pages settings section under "Your site is live at..."

---

## **Custom Domain Setup (Optional)**

If you own a domain (e.g., `finoffer.com`):

1. In **Settings** → **Pages**
2. Under "Custom domain", enter your domain: `finoffer.com`
3. Add CNAME records to your domain registrar:
   - Host: `@` | Type: `A` | Value: `185.199.108.153`
   - Host: `@` | Type: `A` | Value: `185.199.109.153`
   - Host: `@` | Type: `A` | Value: `185.199.110.153`
   - Host: `@` | Type: `A` | Value: `185.199.111.153`

---

## **File Checklist**

✅ Single HTML file with:
- All CSS embedded (no external stylesheets)
- All fonts from Google Fonts CDN
- All icons as inline SVG
- Form validation & submission handling
- Live countdown timer (updates every second)
- Responsive design (mobile, tablet, desktop)
- Dark gold theme (wedding aesthetic)
- Four business segments
- Three pricing tiers
- Pre-booking form with reference ID generation

---

## **What's Included in the HTML**

### **Pages/Sections:**
1. **Hero** - Main value proposition with countdown
2. **Offers** - Four core services (Storage, Dry Cleaning, Rentals, Preloved)
3. **How It Works** - 4-step process strip
4. **Pricing** - Three tier cards (Dulhan Starter, Grand Trousseau, Royal Vault)
5. **Testimonials** - Social proof from customers
6. **Booking Form** - Pre-order with validation & reference ID
7. **Footer** - Brand + links

### **Features:**
- **Live Countdown:** Counts down to 12 May 2025 (updates every second)
- **Form Validation:** Checks all required fields before submission
- **Success Message:** Shows reference ID after booking
- **Smooth Scrolling:** All navigation links animate smoothly
- **Responsive:** Works perfectly on mobile, tablet, desktop
- **No Backend Required:** Works standalone (form data logs to browser console)

---

## **Connect Form to Backend (Optional)**

The form currently logs to console. To capture submissions to email/database:

### **Option 1: FormSubmit.co (Free, No Code)**
Add this to your form tag:
```html
<form action="https://formsubmit.co/your-email@gmail.com" method="POST">
  <!-- form fields unchanged -->
  <input type="hidden" name="_captcha" value="false">
</form>
```

### **Option 2: Netlify Forms**
Deploy to Netlify instead (supports form capture natively)

### **Option 3: Custom Backend**
Connect to your own API endpoint with JavaScript

---

## **Customization Quick Tips**

**Change phone number in footer:**
```javascript
// Find this line in the script:
alert('Contact: +91 9876543210 or hello@fin-india.com')
// Replace with your number
```

**Update company name:**
Search & replace `Fin.India Holdings` with your preferred name

**Change color scheme:**
Edit CSS variables at top of `<style>`:
```css
:root {
  --gold: #C9943A;        /* Main accent color */
  --crimson: #8B1A1A;     /* Urgency/alert color */
  --deep: #1A0A00;        /* Dark background */
}
```

**Modify countdown deadline:**
Change this line:
```javascript
const endDate = new Date('2025-05-12T23:59:59').getTime();
```

---

## **Need Help?**

- **GitHub Pages Docs:** https://pages.github.com
- **HTML File Issues:** Check browser console (F12)
- **Form Not Working:** Try FormSubmit.co integration above
- **Custom Domain:** Contact your domain registrar

---

## **Launch Checklist**

- [ ] Repository created on GitHub
- [ ] `index.html` uploaded to main branch
- [ ] GitHub Pages enabled in Settings
- [ ] Live URL verified & working
- [ ] Form test submission (check console)
- [ ] Countdown timer working
- [ ] Mobile responsiveness checked
- [ ] All links clicking correctly
- [ ] Share live URL with team!

**You're live! 🚀**
