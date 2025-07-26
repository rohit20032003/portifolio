# Content Management Guide
## How to Edit Your Portfolio After Deployment

### ✅ What You CAN Edit Easily

#### 1. **Personal Information**
- **Name & Full Name**: Change "Rohit Kumar" to your name
- **Tagline**: Update your professional tagline/bio
- **Email & Phone**: Update contact information
- **Location**: Change your location
- **Profile Image**: Replace with your photo

#### 2. **About Section**
- **Mission Statement**: Edit your personal mission
- **Values**: Add/edit your core values (title, subtitle, description)
- **Stats**: Update CGPA, internships count, technologies count

#### 3. **Education**
- **Degree**: Change degree name
- **Institution**: Update university/college name
- **Period**: Update graduation years
- **CGPA/Percentage**: Update academic scores

#### 4. **Skills**
- **Programming Languages**: Add/remove languages
- **Tools & Libraries**: Update technical skills
- **Proficiency Levels**: Adjust skill levels (1-10 scale)
- **Categories**: Modify skill categories

#### 5. **Experience**
- **Job Titles**: Update position names
- **Company Names**: Change employer names
- **Duration**: Update work periods
- **Responsibilities**: Edit job descriptions
- **Technologies**: Update tech stacks used

#### 6. **Projects**
- **Project Names**: Change project titles
- **Descriptions**: Update project details
- **Technologies**: Modify tech stacks
- **Features**: Edit project features
- **Status**: Update project status

#### 7. **Contact Information**
- **Contact Intro**: Edit contact section text
- **Social Links**: Update LinkedIn, GitHub, etc.

---

### 🔧 How to Make Changes

#### Method 1: Direct Code Editing (Immediate)
1. Open the file: `server/storage.ts`
2. Find the `defaultPortfolioData` object
3. Edit any values you want to change
4. Save the file
5. The website updates automatically

#### Method 2: API Updates (Advanced)
The website has built-in API endpoints to update content:
- `PUT /api/portfolio/default-user` - Update portfolio data
- You can build an admin panel to edit content via forms

---

### 📝 Example: Changing Your Name

**File**: `server/storage.ts`
**Find this section**:
```javascript
user: {
  name: "Rohit Kumar",
  fullName: "Madagala Rohit Kumar",
  // ... other fields
}
```

**Change to**:
```javascript
user: {
  name: "Your Name",
  fullName: "Your Full Name",
  // ... other fields
}
```

---

### 🚀 After Deployment

#### ✅ Easy to Change:
- All text content (names, descriptions, etc.)
- Contact information
- Skills and proficiency levels
- Project information
- Experience details
- Education information

#### ⚠️ Requires File Upload:
- **Resume PDF**: Replace file in `public/assets/`
- **Profile Images**: Update image files
- **Project Screenshots**: Replace project images

#### 🛠️ Requires Code Changes:
- Website layout/design
- Color schemes
- New sections
- Navigation structure

---

### 💡 Pro Tips

1. **Test Locally First**: Make changes on your development version before updating the live site
2. **Backup**: Keep a copy of your original content
3. **Version Control**: Use Git to track changes
4. **Database**: In production, content is stored in a database, so changes persist

---

### 🎯 Quick Start Checklist

After deployment, update these first:
- [ ] Your name and full name
- [ ] Email and phone number
- [ ] Tagline/bio
- [ ] Replace resume PDF with your actual resume
- [ ] Update education details
- [ ] Add your real work experience
- [ ] Update skills to match your expertise
- [ ] Add your actual projects
- [ ] Update contact information

The portfolio is designed to be easily customizable - you own all the content!