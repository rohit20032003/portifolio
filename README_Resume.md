# How to Add Your Resume

## Quick Setup

1. **Replace the Resume File:**
   - Save your resume as a PDF file
   - Name it `Rohit_Kumar_Resume.pdf` (or update the filename in the code)
   - Replace the file in the `public/assets/` folder

2. **File Location:**
   ```
   public/assets/Rohit_Kumar_Resume.pdf
   ```

3. **The download will work automatically** - when users click "Download Resume", they'll get your actual PDF file.

## Customizing the Filename

If you want to change the filename, update these locations:

1. **Backend route** (`server/routes.ts` line 69 and 78):
   ```javascript
   const resumePath = path.join(process.cwd(), 'public', 'assets', 'YOUR_FILENAME.pdf');
   res.setHeader('Content-Disposition', 'attachment; filename="YOUR_FILENAME.pdf"');
   ```

2. **File location**: Place your PDF in `public/assets/YOUR_FILENAME.pdf`

## Current Features

✅ Automatic PDF download when button is clicked
✅ Proper file headers for browser compatibility
✅ Error handling if file is missing
✅ Works on both hero section and contact section buttons

The resume download feature is now fully functional!