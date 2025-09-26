# Frontend Development - UI Replication Challenge
*A frontend task for those applying for TQ Tech Department*

![Image](./TQ%20Task.png)

## 📌 PRIMARY REQUIREMENT: UI Replication

Your main task is to EXACTLY replicate the UI shown in the provided images - both in Figma design AND in code implementation.

Important: This is a replication challenge. Your goal is to match the design as closely as possible. If you can make it better, that's great - but exact replication is the baseline requirement.

---

##  What You Must Deliver

### 1. Figma Design (Required)
- Create the exact design in Figma first
- Include both desktop and mobile views
- Use the exact colors, fonts, and spacing shown in the images

### 2. Code Implementation (Required)
- Replicate the Figma design exactly in code
- Use any technology stack you prefer (HTML/CSS, Tailwind, React)
- Must match the design
- Include smooth animations for mobile sidebar

---

##  Core Requirements (Mandatory)

### 1. Design Replication
- Reference Images: Study `TQ Task.png`, `Mobile View.png`, and `Mobile View + Sidebar.png`
- Fonts: Use PP Mondwest (heading) and Inter (body text) - fonts provided in `/assets/` For inter use google fonts CDN

- Color Scheme:
  - Web heading: 100px, color #333
  - Body text: 14px, color #444
  - Button text: #fff
  - Sidebar items: #999 (inactive), #444 (active)
  - Mobile heading: 50px
  - Mobile button: 10px text

### 2. Layout Requirements
- Desktop: Use Flexbox and CSS Grid for responsive layout
- Mobile: Implement a collapsible sidebar with smooth animations
- Assets: All images and fonts are provided in `/assets/` directory
- Responsive: Must work seamlessly on desktop, tablet, and mobile devices

### 3. Technical Implementation
- HTML/CSS: Create semantic, accessible markup
- Responsive Design: Use media queries and flexible units
- Animations: Smooth slide-in animation for mobile sidebar (on click)
- Positioning: Use absolute positioning where appropriate for overlay elements

---

## Technology Stack Options

### Option A: Pure HTML/CSS/JS (Recommended for beginners)
- Vanilla HTML5, CSS3 with Flexbox/Grid ans JS
- Focus on CSS animations and transitions

### Option B: Tailwind CSS (Bonus points)
- Use Tailwind CSS utility classes
- Demonstrate modern utility-first approach
- Responsive design with Tailwind's breakpoints

### Option C: React (Maximum bonus points)
- Create React components for reusable UI elements
- Implement state management for sidebar toggle
- Use React hooks for animation control
- Bonus: Deploy to Vercel/Netlify

---

##  Design Specifications

### Desktop Layout
- Header: Large heading (100px, #333) with proper spacing
- Content Area: 14px body text (#444) with appropriate line-height
- Buttons: White text (#fff) on contrasting background
- Grid System: Use CSS Grid for main content layout
- Images: Properly sized and optimized from `/assets/`

### Mobile Layout
- Header: Reduced to 50px heading
- Hamburger Menu: Top-left corner for sidebar toggle
- Sidebar: 
  - Slides in from left with smooth animation
  - Items: #999 for inactive, #444 for active state
  - Overlay backdrop when open
  - Close button or click outside to close
- Buttons: 10px text size for mobile optimization

### Assets Provided
```
assets/
├── asset1.png (19KB)
├── asset2.webp (112KB)
├── asset3.png (45KB)
├── asset4.png (135KB)
├── ppmondwest-regular.otf (PP Mondwest font)
└── ppneuebit-bold.otf (Additional font)
```

---

## Mobile Sidebar Implementation

### Animation Requirements
- Slide-in: Smooth transition from left (-100%) to 0%
- Duration: 300-400ms ease-in-out
- Backdrop: Semi-transparent overlay when sidebar is open
- Close Methods: 
  - Click outside sidebar
  - Close button (X icon)
  - ESC key (optional)

---

## Bonus Points Opportunities

### Design Enhancement
- [ ] Figma Design: Create the design in Figma first (link in README)
- [ ] Dark Mode: Implement dark/light theme toggle
- [ ] Micro-interactions: Hover effects, button animations
- [ ] Accessibility: ARIA labels, keyboard navigation

### Technical Excellence
- [ ] Performance: Optimize images, lazy loading
- [ ] Code Quality: Clean, commented, modular code
- [ ] Cross-browser: Test on Chrome, Firefox, Safari

### Advanced Features
- [ ] React Context: Global state management
- [ ] CSS Modules: Scoped styling
- [ ] Storybook: Component documentation
- [ ] Unit Tests: Jest/React Testing Library



### Responsive Testing
- [ ] 320px: Smallest mobile screen
- [ ] 768px: Tablet portrait
- [ ] 1024px: Tablet landscape/small desktop
- [ ] 1440px: Standard desktop
- [ ] 1920px: Large desktop

### Functionality Testing
- [ ] Sidebar: Opens/closes smoothly on mobile
- [ ] Navigation: All links work correctly
- [ ] Images: Load properly and are responsive
- [ ] Fonts: Render correctly across devices

---

##  Evaluation Criteria

| Criteria | Weight | Notes |
|----------|--------|--------|
| Design Accuracy | 30% | How closely it matches the provided images |
| Responsive Design | 25% | Works well on all screen sizes |
| Code Quality | 20% | Clean, maintainable, well-commented |
| Animation & UX | 15% | Smooth sidebar animation, good user experience |
| Bonus Features | 10% | Tailwind, React, Figma, or other enhancements |

---

## 📚 Resources

### Documentation
- [MDN Flexbox Guide](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout)
- [CSS Grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)
- [Tailwind CSS](https://tailwindcss.com/docs)
- [React Documentation](https://react.dev)

### Tools
- [Figma](https://figma.com) - For design prototyping

---

Remember: This is a REPLICATION CHALLENGE - your primary goal is to match the provided designs exactly. If you can improve upon it while maintaining the core design, that's excellent, but exact replication is the minimum requirement.

Focus on: Pixel-perfect accuracy, exact colors, precise spacing, and identical typography. The closer you get to the original, the better your score will be.