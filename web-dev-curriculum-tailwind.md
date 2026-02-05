# Web Development Learning Path (Tailwind CSS Edition)
## Recreating LA-RIFF Website - A Complete Course

---

## Course Overview

This course teaches you web development using **Tailwind CSS** from the start - the same utility-first framework used in your LA-RIFF website.

**Course Structure:**
- 7 Chapters (HTML → Tailwind → JavaScript → Vite)
- Each chapter: Theory → Examples → Practice Project
- Final project: Complete LA-RIFF website

**What You'll Learn:**
- HTML fundamentals
- Tailwind CSS (utility-first styling)
- Responsive design with Tailwind
- JavaScript basics
- DOM manipulation
- Build tools (Vite)
- Project deployment

---

## Chapter 1: HTML Fundamentals - Building Blocks of the Web

### What is HTML?
HTML (HyperText Markup Language) is the skeleton of every website. It defines the structure and content.

### Core Concepts:

#### 1.1 HTML Document Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Title</title>
</head>
<body>
    <!-- Your content goes here -->
</body>
</html>
```

**Explanation:**
- `<!DOCTYPE html>` - Tells browser this is HTML5
- `<html>` - Root element, wraps everything
- `<head>` - Metadata (not visible on page)
- `<body>` - Visible content

#### 1.2 Essential HTML Tags

**Text Elements:**
```html
<h1>Main Heading</h1>          <!-- Largest heading -->
<h2>Subheading</h2>             <!-- Second level -->
<p>Paragraph text here</p>      <!-- Regular text -->
<span>Inline text</span>        <!-- Small text piece -->
```

**Container Elements:**
```html
<div>Block container</div>       <!-- Block-level box -->
<section>Page section</section>  <!-- Thematic grouping -->
<header>Top of page</header>     <!-- Header area -->
<footer>Bottom of page</footer>  <!-- Footer area -->
<nav>Navigation links</nav>      <!-- Navigation menu -->
```

**Links and Images:**
```html
<a href="https://google.com">Click me</a>
<img src="image.jpg" alt="Description">
```

**Lists:**
```html
<ul>                    <!-- Unordered (bullets) -->
    <li>Item 1</li>
    <li>Item 2</li>
</ul>

<ol>                    <!-- Ordered (numbers) -->
    <li>First</li>
    <li>Second</li>
</ol>
```

#### 1.3 Semantic HTML
Use meaningful tags instead of just `<div>`:
```html
<!-- ❌ Bad -->
<div class="header">
    <div class="nav">...</div>
</div>

<!-- ✅ Good -->
<header>
    <nav>...</nav>
</header>
```

### Chapter 1 Practice Project: "About Me" Page

**Requirements:**
Create a simple personal page with:
1. A header with your name
2. Navigation links (Home, About, Contact)
3. A main section with:
   - Profile image
   - 3 paragraphs about yourself
   - List of 5 hobbies
4. A footer with copyright text

**Starter Code:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About Me</title>
</head>
<body>
    <header>
        <h1>Your Name</h1>
    </header>
    
    <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
    </nav>
    
    <main>
        <img src="profile.jpg" alt="Your Name">
        <p>First paragraph about yourself...</p>
        <p>Second paragraph...</p>
        <p>Third paragraph...</p>
        
        <h2>My Hobbies</h2>
        <ul>
            <li>Hobby 1</li>
            <li>Hobby 2</li>
            <li>Hobby 3</li>
            <li>Hobby 4</li>
            <li>Hobby 5</li>
        </ul>
    </main>
    
    <footer>
        <p>&copy; 2026 Your Name. All rights reserved.</p>
    </footer>
</body>
</html>
```

**Success Criteria:**
- [ ] Page has proper HTML structure
- [ ] All required sections present
- [ ] Uses semantic HTML tags
- [ ] Image has alt text
- [ ] Navigation has at least 3 links

---

## Chapter 2: Tailwind CSS Setup - Getting Started

### What is Tailwind CSS?
Tailwind is a utility-first CSS framework. Instead of writing CSS, you apply pre-made classes directly in your HTML.

**Traditional CSS:**
```html
<div class="card">Hello</div>
```
```css
.card {
    padding: 20px;
    background-color: white;
    border-radius: 8px;
}
```

**Tailwind CSS:**
```html
<div class="p-5 bg-white rounded-lg">Hello</div>
```

### Core Concepts:

#### 2.1 Setting Up Tailwind (CDN Method for Learning)

For now, we'll use the CDN. Later we'll use the proper build setup.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Page</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body>
    <!-- Your Tailwind classes work here! -->
</body>
</html>
```

#### 2.2 Spacing - Padding & Margin

**Padding (space inside element):**
```html
<!-- p-4 = 16px padding on all sides -->
<div class="p-4">Padding all sides</div>

<!-- px-6 = 24px padding left/right -->
<div class="px-6">Padding horizontal</div>

<!-- py-2 = 8px padding top/bottom -->
<div class="py-2">Padding vertical</div>

<!-- pt-8 = 32px padding top only -->
<div class="pt-8">Padding top</div>

<!-- You can also use: pr (right), pb (bottom), pl (left) -->
```

**Spacing Scale:**
- `1` = 4px
- `2` = 8px
- `3` = 12px
- `4` = 16px
- `6` = 24px
- `8` = 32px
- `12` = 48px
- `16` = 64px

**Margin (space outside element):**
```html
<div class="m-4">Margin all sides</div>
<div class="mx-auto">Center horizontally</div>
<div class="mt-6">Margin top</div>
<div class="mb-8">Margin bottom</div>
```

#### 2.3 Colors

**Text Colors:**
```html
<p class="text-black">Black text</p>
<p class="text-white">White text</p>
<p class="text-gray-500">Gray text</p>
<p class="text-red-600">Red text</p>
<p class="text-blue-500">Blue text</p>
```

**Background Colors:**
```html
<div class="bg-black">Black background</div>
<div class="bg-white">White background</div>
<div class="bg-gray-100">Light gray</div>
<div class="bg-blue-500">Blue background</div>
```

**Color Scale (50-950):**
- `50` - Very light
- `100, 200, 300` - Light
- `400, 500, 600` - Medium
- `700, 800, 900` - Dark
- `950` - Very dark

**Opacity:**
```html
<div class="bg-black/50">50% opacity black</div>
<div class="text-white/70">70% opacity white</div>
```

#### 2.4 Typography

**Font Size:**
```html
<p class="text-xs">Extra small (12px)</p>
<p class="text-sm">Small (14px)</p>
<p class="text-base">Base (16px)</p>
<p class="text-lg">Large (18px)</p>
<p class="text-xl">XL (20px)</p>
<p class="text-2xl">2XL (24px)</p>
<p class="text-4xl">4XL (36px)</p>
<p class="text-6xl">6XL (60px)</p>
<p class="text-9xl">9XL (128px)</p>
```

**Font Weight:**
```html
<p class="font-thin">Thin (100)</p>
<p class="font-light">Light (300)</p>
<p class="font-normal">Normal (400)</p>
<p class="font-medium">Medium (500)</p>
<p class="font-semibold">Semibold (600)</p>
<p class="font-bold">Bold (700)</p>
```

**Text Alignment:**
```html
<p class="text-left">Left aligned</p>
<p class="text-center">Center aligned</p>
<p class="text-right">Right aligned</p>
```

**Other Typography:**
```html
<p class="italic">Italic text</p>
<p class="uppercase">UPPERCASE TEXT</p>
<p class="lowercase">lowercase text</p>
<p class="tracking-wide">Letter spacing</p>
<p class="tracking-widest">More letter spacing</p>
<p class="leading-tight">Tight line height</p>
<p class="leading-relaxed">Relaxed line height</p>
```

#### 2.5 Sizing

**Width:**
```html
<div class="w-full">100% width</div>
<div class="w-1/2">50% width</div>
<div class="w-1/3">33.33% width</div>
<div class="w-64">256px width</div>
<div class="w-screen">Full viewport width</div>
```

**Height:**
```html
<div class="h-screen">Full viewport height</div>
<div class="h-64">256px height</div>
<div class="h-full">100% height</div>
```

**Max Width:**
```html
<div class="max-w-7xl">Max 1280px</div>
<div class="max-w-md">Max 448px</div>
<div class="max-w-xs">Max 320px</div>
```

#### 2.6 Borders & Rounded Corners

**Borders:**
```html
<div class="border">1px border</div>
<div class="border-2">2px border</div>
<div class="border-4">4px border</div>
<div class="border-white">White border</div>
<div class="border-white/20">20% opacity white border</div>
```

**Rounded Corners:**
```html
<div class="rounded">4px corners</div>
<div class="rounded-lg">8px corners</div>
<div class="rounded-full">Fully rounded (circle)</div>
<div class="rounded-t-lg">Top corners only</div>
```

### Chapter 2 Practice Project: "Styled About Me"

Take your Chapter 1 HTML and add Tailwind classes!

**Requirements:**
- Add CDN link to `<head>`
- Style header with background color and padding
- Center content with `max-w-` and `mx-auto`
- Style navigation with flex and spacing
- Add rounded corners to image
- Style lists with custom colors
- Add background color to footer

**Example Starter:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About Me</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-50">
    <header class="bg-gradient-to-r from-purple-500 to-pink-500 text-white p-8 text-center">
        <h1 class="text-4xl font-bold">Your Name</h1>
    </header>
    
    <nav class="bg-white shadow-md p-4">
        <div class="max-w-4xl mx-auto flex justify-center gap-8">
            <a href="#home" class="text-gray-700 hover:text-purple-500 transition-colors">Home</a>
            <a href="#about" class="text-gray-700 hover:text-purple-500 transition-colors">About</a>
            <a href="#contact" class="text-gray-700 hover:text-purple-500 transition-colors">Contact</a>
        </div>
    </nav>
    
    <main class="max-w-4xl mx-auto p-8">
        <img src="profile.jpg" alt="Your Name" class="w-64 h-64 rounded-full mx-auto mb-8 object-cover shadow-lg">
        
        <div class="space-y-4 text-gray-700 leading-relaxed">
            <p>First paragraph about yourself...</p>
            <p>Second paragraph...</p>
            <p>Third paragraph...</p>
        </div>
        
        <h2 class="text-3xl font-bold mt-12 mb-6">My Hobbies</h2>
        <ul class="space-y-3">
            <li class="flex items-center">
                <span class="w-2 h-2 bg-purple-500 rounded-full mr-3"></span>
                Hobby 1
            </li>
            <!-- Add more hobbies -->
        </ul>
    </main>
    
    <footer class="bg-gray-800 text-white text-center p-6 mt-12">
        <p>&copy; 2026 Your Name. All rights reserved.</p>
    </footer>
</body>
</html>
```

**Success Criteria:**
- [ ] Tailwind CDN added
- [ ] Uses background colors
- [ ] Text is properly sized and spaced
- [ ] Image has rounded corners
- [ ] Navigation is horizontally aligned
- [ ] Footer has different background

---

## Chapter 3: Flexbox with Tailwind - Layout Made Easy

### What is Flexbox?
Flexbox arranges items in rows or columns with easy alignment. Tailwind makes it super simple!

### Core Concepts:

#### 3.1 Basic Flex Container
```html
<div class="flex">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
</div>
```
Items line up horizontally by default.

#### 3.2 Direction
```html
<!-- Horizontal (default) -->
<div class="flex flex-row">Items →</div>

<!-- Vertical -->
<div class="flex flex-col">
    <div>Item 1</div>
    <div>Item 2</div>
</div>

<!-- Reverse -->
<div class="flex flex-row-reverse">Items ←</div>
<div class="flex flex-col-reverse">Items ↑</div>
```

#### 3.3 Justify Content (Horizontal Alignment)
```html
<!-- Start -->
<div class="flex justify-start">
    [■■■      ]
</div>

<!-- Center -->
<div class="flex justify-center">
    [   ■■■   ]
</div>

<!-- End -->
<div class="flex justify-end">
    [      ■■■]
</div>

<!-- Space between -->
<div class="flex justify-between">
    [■   ■   ■]
</div>

<!-- Space around -->
<div class="flex justify-around">
    [ ■  ■  ■ ]
</div>

<!-- Space evenly -->
<div class="flex justify-evenly">
    [ ■  ■  ■ ]
</div>
```

#### 3.4 Align Items (Vertical Alignment)
```html
<!-- Top -->
<div class="flex items-start h-64">
    Items at top
</div>

<!-- Center -->
<div class="flex items-center h-64">
    Items in middle
</div>

<!-- Bottom -->
<div class="flex items-end h-64">
    Items at bottom
</div>

<!-- Stretch (default) -->
<div class="flex items-stretch h-64">
    Items stretch to fill height
</div>
```

#### 3.5 Gap (Spacing Between Items)
```html
<div class="flex gap-4">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
</div>

<!-- Different gaps -->
<div class="flex gap-2">Small gap</div>
<div class="flex gap-8">Large gap</div>
<div class="flex gap-x-4 gap-y-8">Different horizontal/vertical</div>
```

#### 3.6 Wrap
```html
<!-- Items wrap to next line -->
<div class="flex flex-wrap gap-4">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
    <div>Item 4</div>
    <!-- Wraps if not enough space -->
</div>
```

#### 3.7 Flex Item Properties
```html
<div class="flex">
    <!-- Grow to fill space -->
    <div class="flex-1">Flexible item</div>
    
    <!-- Don't grow -->
    <div>Fixed size</div>
    
    <!-- Specific flex -->
    <div class="flex-none">No grow/shrink</div>
    <div class="flex-auto">Grow based on content</div>
</div>
```

#### 3.8 Common Patterns

**Navbar:**
```html
<nav class="flex justify-between items-center p-6 bg-gray-800 text-white">
    <div class="text-xl font-bold">Logo</div>
    <div class="flex gap-6">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Contact</a>
    </div>
</nav>
```

**Center Everything:**
```html
<div class="flex justify-center items-center h-screen">
    <h1>Perfectly Centered</h1>
</div>
```

**Card Row:**
```html
<div class="flex gap-6">
    <div class="flex-1 bg-white p-6 rounded-lg shadow">Card 1</div>
    <div class="flex-1 bg-white p-6 rounded-lg shadow">Card 2</div>
    <div class="flex-1 bg-white p-6 rounded-lg shadow">Card 3</div>
</div>
```

### Chapter 3 Practice Project: "Product Landing Page"

**Requirements:**
Create a simple product page layout:

1. **Navigation Bar**
   - Logo on left
   - Menu items on right
   - Dark background
   - Items centered vertically

2. **Hero Section**
   - Full viewport height
   - Centered content (v & h)
   - Product name, tagline, button
   - Background color

3. **Features Section**
   - 3 feature cards in a row
   - Each card: icon/emoji, title, description
   - Equal width with gaps
   - Wrap on small screens

4. **Footer**
   - Links on left
   - Copyright on right
   - Dark background

**Starter Code:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Product Page</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body>
    <nav class="YOUR CLASSES">
        <div class="YOUR CLASSES">Brand</div>
        <div class="YOUR CLASSES">
            <a href="#" class="YOUR CLASSES">Home</a>
            <a href="#" class="YOUR CLASSES">Features</a>
            <a href="#" class="YOUR CLASSES">Contact</a>
        </div>
    </nav>
    
    <section class="YOUR CLASSES">
        <div class="YOUR CLASSES">
            <h1 class="YOUR CLASSES">Amazing Product</h1>
            <p class="YOUR CLASSES">The best solution for your needs</p>
            <button class="YOUR CLASSES">Get Started</button>
        </div>
    </section>
    
    <section class="YOUR CLASSES">
        <div class="YOUR CLASSES">
            <div class="YOUR CLASSES">
                <div class="text-4xl mb-4">⚡</div>
                <h3 class="text-xl font-bold mb-2">Fast</h3>
                <p class="text-gray-600">Lightning quick performance</p>
            </div>
            <!-- Add 2 more cards -->
        </div>
    </section>
    
    <footer class="YOUR CLASSES">
        <div class="YOUR CLASSES">Links • About • Contact</div>
        <div class="YOUR CLASSES">&copy; 2026</div>
    </footer>
</body>
</html>
```

**Success Criteria:**
- [ ] Navbar uses flexbox with justify-between
- [ ] Hero content centered with items-center justify-center
- [ ] Features use flex with gap
- [ ] Footer items on opposite sides
- [ ] All spacing done with Tailwind classes
- [ ] No custom CSS needed

---

## Chapter 4: Responsive Design with Tailwind

### What is Responsive Design?
Making websites look good on all screen sizes - phone, tablet, desktop.

### Core Concepts:

#### 4.1 Breakpoint Prefixes

Tailwind uses mobile-first approach. Add prefix for larger screens:

```html
<!-- Always applied -->
<div class="text-sm">Small text</div>

<!-- Small text on mobile, large on tablet+ -->
<div class="text-sm md:text-lg">Responsive text</div>

<!-- Hidden on mobile, flex on desktop -->
<div class="hidden lg:flex">Desktop only</div>
```

**Breakpoints:**
- `sm:` - 640px and up (tablet)
- `md:` - 768px and up (tablet landscape)
- `lg:` - 1024px and up (desktop)
- `xl:` - 1280px and up (large desktop)
- `2xl:` - 1536px and up (extra large)

#### 4.2 Responsive Layout Example
```html
<!-- 1 column mobile, 2 on tablet, 3 on desktop -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
    <div>Card 1</div>
    <div>Card 2</div>
    <div>Card 3</div>
</div>
```

#### 4.3 Responsive Text Sizes
```html
<!-- Grows with screen size -->
<h1 class="text-4xl md:text-6xl lg:text-8xl">
    Big Heading
</h1>

<p class="text-sm md:text-base lg:text-lg">
    Body text
</p>
```

#### 4.4 Responsive Spacing
```html
<!-- Small padding mobile, large on desktop -->
<div class="p-4 md:p-8 lg:p-12">
    Content
</div>

<!-- Stack on mobile, side-by-side on desktop -->
<div class="flex flex-col md:flex-row gap-4">
    <div>Left</div>
    <div>Right</div>
</div>
```

#### 4.5 Show/Hide on Different Screens
```html
<!-- Mobile menu (hidden on desktop) -->
<button class="md:hidden">☰ Menu</button>

<!-- Desktop menu (hidden on mobile) -->
<div class="hidden md:flex gap-6">
    <a href="#">Home</a>
    <a href="#">About</a>
</div>
```

#### 4.6 Responsive Grid
```html
<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
    <!-- 1 col mobile, 2 tablet, 4 desktop -->
    <div class="bg-white p-6 rounded-lg">Item 1</div>
    <div class="bg-white p-6 rounded-lg">Item 2</div>
    <div class="bg-white p-6 rounded-lg">Item 3</div>
    <div class="bg-white p-6 rounded-lg">Item 4</div>
</div>
```

#### 4.7 Container Class
```html
<!-- Responsive max-width container -->
<div class="container mx-auto px-4">
    Content constrained to readable width
</div>
```

### Chapter 4 Practice Project: "Responsive Photo Gallery"

**Requirements:**
Create a responsive image gallery:

**Mobile (< 768px):**
- 1 column
- Full width images
- Vertical navigation
- Large buttons

**Tablet (768px+):**
- 2 columns
- Horizontal navigation

**Desktop (1024px+):**
- 3 columns
- Max width constraint
- Hover effects

**Features:**
1. Gallery title (responsive size)
2. Filter buttons (stack mobile, row desktop)
3. 9 image cards with captions
4. Responsive grid layout

**Starter HTML:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Photo Gallery</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100">
    <header class="bg-white shadow-md p-6 md:p-8">
        <h1 class="text-3xl md:text-5xl lg:text-6xl font-bold text-center mb-6">
            Photo Gallery
        </h1>
        
        <nav class="flex flex-col md:flex-row justify-center gap-2 md:gap-4">
            <button class="bg-blue-500 text-white px-6 py-3 rounded-lg">All</button>
            <button class="bg-gray-200 px-6 py-3 rounded-lg">Nature</button>
            <button class="bg-gray-200 px-6 py-3 rounded-lg">Urban</button>
            <button class="bg-gray-200 px-6 py-3 rounded-lg">People</button>
        </nav>
    </header>
    
    <main class="container mx-auto px-4 py-8">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            <div class="bg-white rounded-lg shadow-md overflow-hidden">
                <img src="photo1.jpg" alt="Photo 1" class="w-full h-64 object-cover">
                <div class="p-4">
                    <p class="text-gray-700">Mountain Landscape</p>
                </div>
            </div>
            <!-- Add 8 more photo cards -->
        </div>
    </main>
</body>
</html>
```

**Success Criteria:**
- [ ] Grid: 1 col mobile, 2 tablet, 3 desktop
- [ ] Title text grows with screen size
- [ ] Buttons stack mobile, row desktop
- [ ] Images scale properly (never overflow)
- [ ] Proper spacing at all sizes
- [ ] Max width on large screens

---

## Chapter 5: CSS Grid with Tailwind - Advanced Layouts

### What is CSS Grid?
A 2-dimensional layout system - control rows AND columns.

### Core Concepts:

#### 5.1 Basic Grid
```html
<div class="grid grid-cols-3 gap-4">
    <div>Column 1</div>
    <div>Column 2</div>
    <div>Column 3</div>
</div>
```

#### 5.2 Column Count
```html
<div class="grid grid-cols-1">1 column</div>
<div class="grid grid-cols-2">2 columns</div>
<div class="grid grid-cols-3">3 columns</div>
<div class="grid grid-cols-4">4 columns</div>
<div class="grid grid-cols-6">6 columns</div>
<div class="grid grid-cols-12">12 columns</div>
```

#### 5.3 Responsive Grid Columns
```html
<!-- 1 mobile, 2 tablet, 4 desktop -->
<div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-4 gap-6">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
    <div>Item 4</div>
</div>
```

#### 5.4 Column Spanning
```html
<div class="grid grid-cols-3 gap-4">
    <!-- Spans 2 columns -->
    <div class="col-span-2">Wide item</div>
    <div>Normal</div>
    
    <!-- Spans all 3 columns -->
    <div class="col-span-3">Full width</div>
</div>
```

#### 5.5 Row Spanning
```html
<div class="grid grid-cols-3 grid-rows-2 gap-4">
    <!-- Spans 2 rows -->
    <div class="row-span-2">Tall item</div>
    <div>Normal</div>
    <div>Normal</div>
    <div>Normal</div>
    <div>Normal</div>
</div>
```

#### 5.6 Auto-Fill Pattern
```html
<!-- Automatically creates columns that fit -->
<div class="grid grid-cols-[repeat(auto-fit,minmax(250px,1fr))] gap-4">
    <div>Card 1</div>
    <div>Card 2</div>
    <div>Card 3</div>
    <!-- Wraps automatically based on space -->
</div>
```

#### 5.7 Common Layouts

**Sidebar Layout:**
```html
<div class="grid md:grid-cols-[250px_1fr] gap-6 h-screen">
    <aside class="bg-gray-800 text-white p-6">
        Sidebar (fixed width)
    </aside>
    <main class="bg-white p-6">
        Main content (flexible)
    </main>
</div>
```

**Dashboard Layout:**
```html
<div class="grid grid-cols-12 gap-4">
    <!-- Spans 8 columns (main) -->
    <div class="col-span-12 md:col-span-8 bg-white p-6">
        Main content
    </div>
    
    <!-- Spans 4 columns (sidebar) -->
    <div class="col-span-12 md:col-span-4 bg-white p-6">
        Sidebar
    </div>
</div>
```

**Magazine Layout:**
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
    <!-- Feature article spans 2 columns -->
    <article class="md:col-span-2 lg:col-span-2 bg-white p-6">
        Featured Story
    </article>
    
    <!-- Sidebar -->
    <aside class="bg-gray-100 p-6">
        Related
    </aside>
    
    <!-- Regular articles -->
    <article class="bg-white p-6">Article 1</article>
    <article class="bg-white p-6">Article 2</article>
    <article class="bg-white p-6">Article 3</article>
</div>
```

### Chapter 5 Practice Project: "Blog Layout"

**Requirements:**
Create a blog layout using Grid:

**Desktop Layout:**
```
┌─────────────────────────────────────┐
│           Header (full width)        │
├──────────┬──────────────────────────┤
│          │                          │
│ Sidebar  │      Main Content        │
│ (fixed)  │      (flexible)          │
│          │                          │
│          │  ┌──────┐  ┌──────┐     │
│          │  │ Card │  │ Card │     │
│          │  └──────┘  └──────┘     │
├──────────┴──────────────────────────┤
│           Footer (full width)        │
└─────────────────────────────────────┘
```

**Mobile:** Stack everything vertically

**Starter Code:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Blog</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100">
    <div class="min-h-screen grid grid-rows-[auto_1fr_auto] md:grid-cols-[250px_1fr]">
        <!-- Header spans all columns -->
        <header class="bg-white shadow-md p-6 md:col-span-2">
            <h1 class="text-3xl font-bold">My Blog</h1>
        </header>
        
        <!-- Sidebar -->
        <aside class="bg-white p-6 md:row-start-2">
            <div class="mb-8">
                <img src="avatar.jpg" alt="Author" class="w-24 h-24 rounded-full mx-auto mb-4">
                <h3 class="text-xl font-bold text-center">John Doe</h3>
                <p class="text-gray-600 text-center">Writer & Developer</p>
            </div>
            
            <div>
                <h4 class="font-bold mb-3">Categories</h4>
                <ul class="space-y-2 text-gray-600">
                    <li>Web Development</li>
                    <li>Design</li>
                    <li>Tutorials</li>
                </ul>
            </div>
        </aside>
        
        <!-- Main content -->
        <main class="p-6 md:row-start-2">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <article class="bg-white rounded-lg shadow-md overflow-hidden">
                    <img src="post1.jpg" alt="Post" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h2 class="text-2xl font-bold mb-2">First Blog Post</h2>
                        <p class="text-gray-600 mb-4">This is a preview...</p>
                        <a href="#" class="text-blue-500 hover:underline">Read More →</a>
                    </div>
                </article>
                <!-- Add 5 more post cards -->
            </div>
        </main>
        
        <!-- Footer spans all columns -->
        <footer class="bg-gray-800 text-white text-center p-6 md:col-span-2">
            <p>&copy; 2026 My Blog. All rights reserved.</p>
        </footer>
    </div>
</body>
</html>
```

**Success Criteria:**
- [ ] Uses grid layout
- [ ] Sidebar fixed width on desktop
- [ ] Post cards in 2-column grid
- [ ] Stacks vertically on mobile
- [ ] Header and footer span full width
- [ ] Proper gap spacing

---

## Chapter 6: JavaScript Basics - Making Pages Interactive

### What is JavaScript?
JavaScript makes websites interactive - clicking buttons, showing/hiding content, loading data.

### Core Concepts:

#### 6.1 Variables
```javascript
// let - can be changed
let age = 25;
age = 26;  // OK

// const - cannot be changed
const name = "John";
name = "Jane";  // ERROR

// Always use const unless you need to change the value
```

#### 6.2 Data Types
```javascript
// String (text)
const text = "Hello";
const text2 = 'World';

// Number
const age = 25;
const price = 19.99;

// Boolean
const isActive = true;
const isLoggedIn = false;

// Array (list)
const colors = ["red", "blue", "green"];
console.log(colors[0]);  // "red"

// Object (key-value pairs)
const person = {
    name: "John",
    age: 25,
    city: "NYC"
};
console.log(person.name);  // "John"
```

#### 6.3 Functions
```javascript
// Arrow function (modern way)
const greet = (name) => {
    return "Hello, " + name;
}
greet("John");  // "Hello, John"

// Short arrow function (one line)
const greet = name => `Hello, ${name}`;
```

#### 6.4 DOM Manipulation

**Selecting Elements:**
```javascript
// Get element by ID
const header = document.getElementById('header');

// Get element by CSS selector
const button = document.querySelector('.btn');
const allButtons = document.querySelectorAll('.btn');
```

**Changing Content:**
```javascript
// Change text
const title = document.querySelector('h1');
title.textContent = "New Title";

// Change HTML
const container = document.querySelector('.container');
container.innerHTML = '<p>New content</p>';
```

**Changing Tailwind Classes:**
```javascript
const box = document.querySelector('.box');

// Add classes
box.classList.add('bg-blue-500', 'text-white');

// Remove classes
box.classList.remove('hidden');

// Toggle class (on/off)
box.classList.toggle('hidden');
```

**Event Listeners:**
```javascript
const button = document.querySelector('button');

// Click event
button.addEventListener('click', () => {
    console.log('Button clicked!');
});

// Input event
const input = document.querySelector('input');
input.addEventListener('input', (e) => {
    console.log('User typed:', e.target.value);
});
```

#### 6.5 Common Patterns with Tailwind

**Toggle Menu:**
```javascript
const menuBtn = document.querySelector('#menu-btn');
const nav = document.querySelector('#mobile-nav');

menuBtn.addEventListener('click', () => {
    nav.classList.toggle('hidden');
});
```

**Show/Hide Modal:**
```javascript
const modal = document.querySelector('#modal');
const openBtn = document.querySelector('#open-modal');
const closeBtn = document.querySelector('#close-modal');

openBtn.addEventListener('click', () => {
    modal.classList.remove('hidden');
});

closeBtn.addEventListener('click', () => {
    modal.classList.add('hidden');
});
```

**Dynamic Content:**
```javascript
const products = [
    { name: "Shirt", price: 29.99 },
    { name: "Pants", price: 49.99 }
];

const container = document.querySelector('#products');

products.forEach(product => {
    const html = `
        <div class="bg-white p-6 rounded-lg shadow-md">
            <h3 class="text-xl font-bold">${product.name}</h3>
            <p class="text-gray-600">$${product.price}</p>
        </div>
    `;
    container.innerHTML += html;
});
```

### Chapter 6 Practice Project: "Interactive Todo List"

**Requirements:**
Build a todo list with JavaScript and Tailwind:

**Features:**
1. Input field to add new todos
2. Button to add todo
3. Display todos in a list
4. Each todo has:
   - Checkbox to mark complete
   - Delete button
5. Completed todos have line-through
6. Count of total todos

**Starter HTML:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Todo List</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100 p-8">
    <div class="max-w-md mx-auto bg-white rounded-lg shadow-lg p-6">
        <h1 class="text-3xl font-bold mb-6">My Todo List</h1>
        
        <div class="flex gap-2 mb-6">
            <input 
                type="text" 
                id="todoInput"
                placeholder="Add a new task..."
                class="flex-1 border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
            >
            <button 
                id="addBtn"
                class="bg-blue-500 text-white px-6 py-2 rounded-lg hover:bg-blue-600 transition-colors"
            >
                Add
            </button>
        </div>
        
        <p class="text-sm text-gray-600 mb-4">
            Total: <span id="todoCount" class="font-bold">0</span> tasks
        </p>
        
        <ul id="todoList" class="space-y-2">
            <!-- Todos will be added here -->
        </ul>
    </div>
    
    <script>
        const todoInput = document.getElementById('todoInput');
        const addBtn = document.getElementById('addBtn');
        const todoList = document.getElementById('todoList');
        const todoCount = document.getElementById('todoCount');
        
        let todos = [];
        
        function addTodo() {
            const text = todoInput.value.trim();
            if (text === '') return;
            
            todos.push({
                id: Date.now(),
                text: text,
                completed: false
            });
            
            todoInput.value = '';
            renderTodos();
        }
        
        function deleteTodo(id) {
            todos = todos.filter(todo => todo.id !== id);
            renderTodos();
        }
        
        function toggleTodo(id) {
            todos = todos.map(todo => 
                todo.id === id ? { ...todo, completed: !todo.completed } : todo
            );
            renderTodos();
        }
        
        function renderTodos() {
            todoList.innerHTML = todos.map(todo => `
                <li class="flex items-center gap-3 p-3 bg-gray-50 rounded-lg">
                    <input 
                        type="checkbox" 
                        ${todo.completed ? 'checked' : ''}
                        onchange="toggleTodo(${todo.id})"
                        class="w-5 h-5"
                    >
                    <span class="flex-1 ${todo.completed ? 'line-through text-gray-400' : ''}">
                        ${todo.text}
                    </span>
                    <button 
                        onclick="deleteTodo(${todo.id})"
                        class="text-red-500 hover:text-red-700 font-bold"
                    >
                        ✕
                    </button>
                </li>
            `).join('');
            
            todoCount.textContent = todos.length;
        }
        
        addBtn.addEventListener('click', addTodo);
        todoInput.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') addTodo();
        });
    </script>
</body>
</html>
```

**Success Criteria:**
- [ ] Can add new todos
- [ ] Can mark todos complete (line-through)
- [ ] Can delete todos
- [ ] Count updates correctly
- [ ] Input clears after adding
- [ ] Enter key works
- [ ] Uses Tailwind for all styling

---

## Chapter 7: Vite + Tailwind - Professional Setup

### What is Vite?
Vite is a build tool that provides:
- Instant dev server
- Hot reload (see changes instantly)
- Production optimization
- Proper Tailwind setup

### Setting Up a Real Project:

#### Step 1: Create Project Structure
```bash
mkdir my-project
cd my-project
npm init -y
```

#### Step 2: Install Dependencies
```bash
npm install vite @tailwindcss/vite tailwindcss
```

#### Step 3: Create Configuration Files

**package.json:**
```json
{
  "name": "my-project",
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview"
  },
  "dependencies": {
    "@tailwindcss/vite": "^4.1.18",
    "tailwindcss": "^4.1.18",
    "vite": "^7.3.1"
  }
}
```

**vite.config.js:**
```javascript
import { defineConfig } from 'vite'
import tailwindcss from '@tailwindcss/vite'

export default defineConfig({
  plugins: [tailwindcss()],
})
```

#### Step 4: Create Project Files

**File Structure:**
```
my-project/
├── index.html
├── package.json
├── vite.config.js
├── src/
│   ├── main.js
│   ├── style.css
│   └── products.js
└── public/
    └── images/
```

**index.html:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Project</title>
</head>
<body>
    <div id="app"></div>
    <script type="module" src="/src/main.js"></script>
</body>
</html>
```

**src/style.css:**
```css
@import "tailwindcss";
```

**src/main.js:**
```javascript
import './style.css'

console.log('Hello from Vite!');
```

#### Step 5: Run Development Server
```bash
npm run dev
```
Opens at http://localhost:5173

#### Step 6: Build for Production
```bash
npm run build
```
Creates optimized `dist/` folder

### Chapter 7 Practice Project: "LA-RIFF Simplified"

**Requirements:**
Build a simplified version of LA-RIFF using proper Vite + Tailwind setup:

**Features:**
1. Hero section with background
2. Product grid (load from JS array)
3. Hover effects on products
4. Responsive layout
5. Proper build setup

**Step-by-Step:**

1. **Create project:**
```bash
mkdir la-riff-simple
cd la-riff-simple
npm init -y
npm install vite @tailwindcss/vite tailwindcss
```

2. **Create vite.config.js:**
```javascript
import { defineConfig } from 'vite'
import tailwindcss from '@tailwindcss/vite'

export default defineConfig({
  plugins: [tailwindcss()],
})
```

3. **Create src/products.js:**
```javascript
export const products = [
    {
        id: 1,
        name: "Shadow Hoodie",
        price: 89.99,
        image: "/images/hoodie.jpg"
    },
    {
        id: 2,
        name: "Noir Denim",
        price: 129.99,
        image: "/images/denim.jpg"
    },
    {
        id: 3,
        name: "Urban Jacket",
        price: 159.99,
        image: "/images/jacket.jpg"
    }
];
```

4. **Create index.html:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LA RIFF Simple</title>
</head>
<body class="bg-black text-white">
    <!-- Nav -->
    <nav class="fixed top-0 w-full px-6 py-4 flex justify-between items-center bg-black/50 backdrop-blur z-50">
        <div class="text-xl font-bold tracking-widest">LA RIFF</div>
        <div class="hidden md:flex gap-8 text-sm uppercase">
            <a href="#" class="hover:opacity-70 transition-opacity">Collection</a>
            <a href="#" class="hover:opacity-70 transition-opacity">Cart</a>
        </div>
    </nav>
    
    <!-- Hero -->
    <header class="h-screen flex items-center justify-center relative">
        <div class="absolute inset-0 bg-gradient-to-b from-black/50 to-black"></div>
        <div class="relative z-10 text-center">
            <h1 class="text-7xl md:text-9xl font-bold mb-4">LA RIFF</h1>
            <p class="text-xl italic tracking-widest">Fashion, Redefined.</p>
        </div>
    </header>
    
    <!-- Products -->
    <section class="px-6 py-24">
        <h2 class="text-4xl md:text-6xl font-bold mb-16 text-center">The Collection</h2>
        <div id="product-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-7xl mx-auto">
            <!-- Products injected here -->
        </div>
    </section>
    
    <script type="module" src="/src/main.js"></script>
</body>
</html>
```

5. **Create src/main.js:**
```javascript
import './style.css'
import { products } from './products.js'

const productGrid = document.getElementById('product-grid');

products.forEach(product => {
    const card = `
        <div class="group cursor-pointer">
            <div class="aspect-square bg-zinc-900 mb-4 overflow-hidden rounded-lg">
                <img 
                    src="${product.image}" 
                    alt="${product.name}"
                    class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all duration-500 group-hover:scale-110"
                >
            </div>
            <h3 class="text-xl mb-2">${product.name}</h3>
            <p class="text-gray-400">$${product.price.toFixed(2)}</p>
        </div>
    `;
    productGrid.innerHTML += card;
});
```

6. **Create src/style.css:**
```css
@import "tailwindcss";
```

7. **Run:**
```bash
npm run dev
```

**Success Criteria:**
- [ ] Dev server runs
- [ ] Tailwind classes work
- [ ] Products load from JS
- [ ] Hover effects work
- [ ] Responsive layout
- [ ] Can build for production

---

## FINAL PROJECT: Complete LA-RIFF Website

Now combine everything you've learned!

### Project Requirements:

**Pages:**
1. **Home (index.html)** - Hero + Product grid
2. **Product Detail (product-detail.html)** - Product info + Add to cart
3. **Products (products.html)** - Filters + Sorting

**Technical Stack:**
- ✅ Vite build setup
- ✅ Tailwind CSS (NO custom CSS files)
- ✅ Responsive (mobile-first)
- ✅ JavaScript for interactivity
- ✅ Modular code structure

### Recommended Timeline:

**Week 1-2:** Setup + Home Page
**Week 3-4:** Product Grid + Data
**Week 5-6:** Product Detail Page
**Week 7-8:** Filters, Cart, Polish

---

## Your Learning Checklist

### Chapter 1 - HTML ✅
- [ ] Completed "About Me" page
- [ ] Understand HTML structure
- [ ] Can use semantic tags

### Chapter 2 - Tailwind Setup ✅
- [ ] Added CDN to project
- [ ] Understand utility classes
- [ ] Can style with Tailwind

### Chapter 3 - Flexbox ✅
- [ ] Completed "Product Landing"
- [ ] Can center elements
- [ ] Can create layouts with flex

### Chapter 4 - Responsive ✅
- [ ] Completed "Photo Gallery"
- [ ] Understand breakpoints (sm, md, lg)
- [ ] Can make mobile-first designs

### Chapter 5 - Grid ✅
- [ ] Completed "Blog Layout"
- [ ] Can create complex layouts
- [ ] Understand column spanning

### Chapter 6 - JavaScript ✅
- [ ] Completed "Todo List"
- [ ] Can manipulate DOM
- [ ] Can add Tailwind classes with JS

### Chapter 7 - Vite ✅
- [ ] Completed "LA-RIFF Simplified"
- [ ] Can set up projects
- [ ] Can build for production

### Final Project ✅
- [ ] Complete LA-RIFF website
- [ ] Deployed online
- [ ] Portfolio ready!

---

## Tailwind Quick Reference

### Spacing
```
p-4    padding: 16px
px-6   padding-left/right: 24px
py-2   padding-top/bottom: 8px
m-4    margin: 16px
mx-auto  margin-left/right: auto (center)
```

### Colors
```
bg-black  text-white  border-gray-500
bg-blue-500  text-red-600  bg-black/50 (opacity)
```

### Typography
```
text-sm  text-base  text-lg  text-2xl  text-6xl
font-light  font-normal  font-bold
uppercase  italic  tracking-wide
```

### Layout
```
flex  flex-col  justify-center  items-center  gap-4
grid  grid-cols-3  gap-6
```

### Sizing
```
w-full  w-1/2  w-64  h-screen  h-64
max-w-7xl  max-w-md
```

### Effects
```
hover:opacity-70  transition-colors  duration-500
rounded-lg  shadow-md  border  border-2
```

### Responsive
```
md:text-lg   (768px+)
lg:grid-cols-3   (1024px+)
hidden  md:flex  (hide mobile, show tablet+)
```

---

**Good luck! Build each project completely before moving on. Tailwind makes styling fast and fun! 🚀**
