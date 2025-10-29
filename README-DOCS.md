# SASS Exercise Documentation

## Project Structure

```
epicode-S6-L3-SASS_I/
├── scss/
│   ├── partials/
│   │   ├── _reset.scss        # Reset styles
│   │   ├── _colors.scss       # Color variables
│   │   ├── _fonts.scss        # Font variables and title-big mixin
│   │   ├── _spacings.scss     # Dynamic spacing classes
│   │   ├── _buttons.scss      # Dynamic button classes
│   │   ├── _mixins.scss       # Floating and grid mixins
│   │   └── _animations.scss   # Fade-slide-in animation mixin
│   └── style.scss             # Main SASS file
├── css/
│   └── style.css              # Compiled CSS
├── index.html                 # Demo HTML
├── package.json               # NPM configuration
└── README-DOCS.md             # This documentation
```

## SASS Features Implemented

### 1. Variables

- **Colors**: Text, background, button colors defined in `_colors.scss`
- **Font sizes**: Responsive scale from xs (12px) to hero (48px)
- **Font weights**: Light to black variations
- **Spacings**: From sm (8px) to xxl (64px)

### 2. Dynamic Class Generation

- **Spacing classes**: `padding-block/inline-{size}` and `margin-block/inline-{size}`
- **Button classes**: `btn-primary`, `btn-secondary`, `btn-success` generated from color map

### 3. Mixins

#### `title-big`

```scss
@include title-big;
```

Used for the main hero title with large font size and bold weight.

#### `floating($border-radius, $shadow, $border)`

```scss
@include floating(1rem, 0 15px 40px $shadow-dark, 3px solid $light-border);
```

Creates elevated appearance with shadow and optional border. Used for:

- Hero image (with border)
- Grid images (without border)

#### `grid($columns, $gap)`

```scss
@include grid(4, 2rem);
```

Creates flexible grid layout with specified columns and gap.

#### `fade-slide-in($duration, $delay, $start-position, $end-position, $animation-name)`

```scss
@include fade-slide-in(1s, 0.2s, -30px, 0, heroTitle);
```

Creates unique fade-in with slide-down animation for each element.

### 4. Animation Implementation

All hero elements use staggered animations:

- Hero title: 0.2s delay
- Hero description: 0.4s delay
- Hero buttons: 0.6s delay
- Hero image: 0.8s delay

Each animation has a unique keyframe name to avoid conflicts.

### 5. Responsive Design

- **Desktop**: 4-column grid, side-by-side hero layout
- **Tablet (≤768px)**: 2-column grid, stacked hero layout
- **Mobile (≤480px)**: 1-column grid, smaller fonts, vertical buttons

## Color Scheme

- **Text**: `#f4f4f4` (Light gray)
- **Hero Background**: `#640fc5` (Purple gradient)
- **Buttons**:
  - Primary: `#0e6cff` (Blue)
  - Secondary: `#ff8700` (Orange)
  - Success: `#4caf50` (Green)

## How to Compile SASS

### Option 1: Using npm scripts (recommended)

```bash
npm install
npm run sass          # Single compilation
npm run sass:watch     # Watch mode
npm run sass:compressed # Minified output
```

### Option 2: Direct SASS command

```bash
sass scss/style.scss css/style.css
```

## Features Demonstrated

✅ **Reset styles** in separate partial  
✅ **Color variables** with button color map  
✅ **Font variables** with responsive scale  
✅ **Dynamic spacing classes** using loops  
✅ **Dynamic button classes** from color map  
✅ **Floating mixin** with optional parameters  
✅ **Grid mixin** for flexible layouts  
✅ **Animation mixin** with unique keyframes  
✅ **Proper partial organization**  
✅ **Responsive design**  
✅ **Modern CSS properties** (grid, flexbox, transforms)

## Browser Support

- Modern browsers supporting CSS Grid and Flexbox
- CSS animations and transforms
- CSS custom properties (not used but structure supports)

## Next Steps

To extend this project:

1. Add more color themes
2. Implement dark/light mode toggle
3. Add more animation variations
4. Create additional layout mixins
5. Add form components with consistent styling
