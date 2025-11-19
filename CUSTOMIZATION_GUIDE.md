# Website Customization Guide

This guide will help you personalize your portfolio website. All changes are made in `index.html` unless otherwise specified.

## 📝 Quick Edits Checklist

- [ ] Update name and title
- [ ] Change email and social links
- [ ] Add resume PDF
- [ ] Update about section
- [ ] Add your experience
- [ ] List your skills
- [ ] Add your projects
- [ ] Add publications (if any)
- [ ] Update education details
- [ ] Customize colors (optional)

---

## 1. Personal Information

### Your Name & Title (Lines 30-50)

**Find:**
```html
<h1 class="hero-title">Sashwat Bilvesh Desai</h1>
<p class="hero-description">MS Applied Mathematics @ Northeastern University</p>
```

**Change to:**
```html
<h1 class="hero-title">Your Full Name</h1>
<p class="hero-description">Your Degree @ Your University</p>
```

### Animated Roles (js/main.js, Line 50)

**Find:**
```javascript
const textArray = [
    'Applied Mathematics',
    'Machine Learning',
    'Data Science',
    'Mathematical Modeling',
    'Research & Innovation'
];
```

**Change to your roles:**
```javascript
const textArray = [
    'Your Field 1',
    'Your Field 2',
    'Your Field 3'
];
```

---

## 2. Contact Information

### Email (Multiple locations - Lines 47, 340, 375)

**Find all instances of:**
```html
desai.s@northeastern.edu
```

**Replace with:**
```html
your.email@example.com
```

### LinkedIn (Lines 345, 376)

**Find:**
```html
https://linkedin.com/in/sashwat-desai
```

**Replace with:**
```html
https://linkedin.com/in/your-profile
```

### GitHub (Lines 350, 377)

**Find:**
```html
https://github.com/sashwatdesai
```

**Replace with:**
```html
https://github.com/your-username
```

---

## 3. About Section (Lines 55-65)

Replace the three paragraphs with your own story:

```html
<p>Your first paragraph about your background...</p>
<p>Your second paragraph about research interests...</p>
<p>Your third paragraph about experience...</p>
```

**Tips:**
- Keep it concise (3-4 sentences per paragraph)
- Highlight your unique strengths
- Mention key achievements

---

## 4. Experience Section (Lines 70-110)

### Edit Existing Experience

**Find each experience block:**
```html
<div class="timeline-item">
    <div class="timeline-marker"></div>
    <div class="timeline-content">
        <h3>Job Title</h3>
        <h4>Company Name</h4>
        <p class="timeline-date">Date Range</p>
        <p>Description of your role and achievements...</p>
    </div>
</div>
```

### Add New Experience

Copy the entire `timeline-item` block and paste it within the `<div class="timeline">` section.

---

## 5. Skills Section (Lines 115-180)

### Edit Existing Skills

**Find skill items like:**
```html
<div class="skill-item">
    <i class="devicon-python-plain colored"></i>
    <span>Python</span>
</div>
```

**Change the icon and name to match your skills.**

### Add New Skills

1. Visit [Devicon](https://devicon.dev/) to find your technology icon
2. Copy a skill-item block
3. Replace icon class and name

**Example for JavaScript:**
```html
<div class="skill-item">
    <i class="devicon-javascript-plain colored"></i>
    <span>JavaScript</span>
</div>
```

### Remove Skills

Simply delete the entire `<div class="skill-item">...</div>` block.

---

## 6. Projects Section (Lines 185-250)

### Edit Project

**Find:**
```html
<div class="project-card">
    <div class="project-icon">
        <i class="fas fa-theater-masks"></i>
    </div>
    <h3>Project Name</h3>
    <p>Project description...</p>
    <div class="project-tags">
        <span class="tag">Tech 1</span>
        <span class="tag">Tech 2</span>
    </div>
    <a href="#" class="project-link">View Project <i class="fas fa-arrow-right"></i></a>
</div>
```

**Update:**
- Icon (find icons at [Font Awesome](https://fontawesome.com/icons))
- Project name
- Description
- Tags (technologies used)
- Link (GitHub repo or live demo)

### Add New Project

Copy entire `project-card` block and paste within `<div class="projects-grid">`.

---

## 7. Publications Section (Lines 255-285)

### Edit Publication

```html
<div class="publication-item">
    <div class="publication-icon">
        <i class="fas fa-file-alt"></i>
    </div>
    <div class="publication-content">
        <h3>Paper Title</h3>
        <p class="publication-authors">Your Name, Co-authors</p>
        <p class="publication-venue">Conference/Journal Name, Year</p>
        <p class="publication-details">Brief description of the paper...</p>
        <a href="https://link-to-paper.com" class="publication-link">
            Read Paper <i class="fas fa-external-link-alt"></i>
        </a>
    </div>
</div>
```

### No Publications Yet?

Delete the entire Publications section (Lines 253-287) or hide it by adding `style="display: none;"` to the section tag:

```html
<section id="publications" class="section" style="display: none;">
```

---

## 8. Education Section (Lines 290-330)

### Edit Degree

```html
<div class="education-card">
    <div class="education-icon">
        <i class="fas fa-graduation-cap"></i>
    </div>
    <h3>Your Degree Name</h3>
    <h4>Your University</h4>
    <p class="education-date">Start Year - End Year (or "Present")</p>
    <p class="education-description">Brief description of your program...</p>
    <div class="education-courses">
        <span class="course-tag">Course 1</span>
        <span class="course-tag">Course 2</span>
        <span class="course-tag">Course 3</span>
    </div>
</div>
```

**Update:**
- Degree name
- University name
- Dates
- Description
- Relevant courses

---

## 9. Adding Your Resume

### Step 1: Add PDF File
1. Place your resume PDF in the `assets/resume/` folder
2. Name it `resume.pdf`

### Step 2: Update Link (if different name)

If your file has a different name, update line 47:

```html
<a href="assets/resume/your-resume-name.pdf" download class="btn btn-secondary">
```

---

## 10. Customizing Colors (Optional)

Open `css/main.css` and edit lines 2-10:

```css
:root {
    --primary-color: #1e3a8a;      /* Main color (navy blue) */
    --secondary-color: #14b8a6;    /* Accent color (teal) */
    --accent-color: #f97316;       /* Highlight color (orange) */
}
```

**Change the hex codes to your preferred colors.**

Use [Coolors](https://coolors.co/) to find color combinations.

---

## 11. Footer Copyright (Line 372)

```html
<p>&copy; 2024 Your Name. All rights reserved.</p>
```

Update the year and name.

---

## 🚀 Publishing Your Website

### Option 1: GitHub Pages (Free)
1. Create a GitHub repository
2. Upload all files
3. Go to Settings → Pages
4. Select main branch → Save
5. Your site will be live at `https://yourusername.github.io/repository-name`

### Option 2: Netlify (Free)
1. Go to [Netlify](https://www.netlify.com/)
2. Drag and drop your project folder
3. Site goes live instantly

### Option 3: Vercel (Free)
1. Go to [Vercel](https://vercel.com/)
2. Import your GitHub repository
3. Deploy with one click

---

## 💡 Tips

- **Test locally**: Open `index.html` in your browser before publishing
- **Mobile check**: Test on your phone to ensure responsiveness
- **Proofread**: Check for typos in all sections
- **Links**: Make sure all external links work
- **Images**: Optimize images for web (compress them)

---

## ❓ Need Help?

- **Icons**: [Font Awesome](https://fontawesome.com/icons) | [Devicons](https://devicon.dev/)
- **Colors**: [Coolors](https://coolors.co/) | [Adobe Color](https://color.adobe.com/)
- **Fonts**: [Google Fonts](https://fonts.google.com/)

---

**Good luck with your portfolio! 🎉**
