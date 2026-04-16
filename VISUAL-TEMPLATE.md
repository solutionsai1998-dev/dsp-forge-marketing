# DSP Forge Visual Design Template
## Comprehensive Style Guide — April 15, 2026

Combining competitor research + subagent suggestions + alternative patterns

---

## 1. COLOR SYSTEM

### Primary Palette
```css
:root {
  /* Brand Core */
  --brand-primary: #0ea5e9;      /* Teal-500 — differentiates from blue competitors */
  --brand-secondary: #8b5cf6;    /* Violet-500 — friendly, modern */
  --brand-accent: #f97316;       /* Orange-500 — energy, action */
  
  /* Dark Mode (Default) */
  --bg-primary: #0a0f1a;         /* Deepest navy */
  --bg-secondary: #111827;       /* Card backgrounds */
  --bg-tertiary: #1f2937;        /* Elevated surfaces */
  --bg-elevated: #374151;        /* Hover states */
  
  /* Text */
  --text-primary: #f9fafb;       /* White-ish */
  --text-secondary: #9ca3af;     /* Muted gray */
  --text-tertiary: #6b7280;      /* Very muted */
  
  /* Borders */
  --border-subtle: rgba(148, 163, 184, 0.1);
  --border-default: rgba(148, 163, 184, 0.2);
  --border-focus: rgba(14, 165, 233, 0.5);
  
  /* Status */
  --status-red: #ef4444;
  --status-yellow: #f59e0b;
  --status-green: #22c55e;
  --status-blue: #3b82f6;
}
```

### Gradient Patterns
```css
/* Hero gradient text */
.gradient-text {
  background: linear-gradient(135deg, #f9fafb 0%, #0ea5e9 50%, #8b5cf6 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

/* CTA button gradient */
.gradient-cta {
  background: linear-gradient(135deg, #0ea5e9 0%, #8b5cf6 100%);
}

/* Subtle card gradient overlay */
.card-gradient {
  background: linear-gradient(180deg, rgba(255,255,255,0.03) 0%, transparent 100%);
}

/* Aurora background effect */
.aurora-bg {
  background: 
    radial-gradient(ellipse 80% 50% at 20% 40%, rgba(14, 165, 233, 0.15), transparent),
    radial-gradient(ellipse 60% 40% at 80% 60%, rgba(139, 92, 246, 0.1), transparent);
}
```

---

## 2. TYPOGRAPHY

### Font Stack
```css
/* Modern, clean sans-serif */
--font-primary: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
--font-mono: 'JetBrains Mono', 'Fira Code', monospace; /* For numbers/data */
```

### Type Scale
```css
/* Marketing Site */
--text-hero: 3.5rem;      /* 56px — H1 headlines */
--text-display: 2.5rem;   /* 40px — Section headers */
--text-title: 1.5rem;     /* 24px — Card titles */
--text-body: 1rem;        /* 16px — Body text */
--text-small: 0.875rem;   /* 14px — Captions, labels */
--text-xs: 0.75rem;       /* 12px — Fine print */

/* Product App */
--app-header: 1.25rem;    /* 20px */
--app-title: 1rem;        /* 16px */
--app-body: 0.875rem;     /* 14px */
--app-small: 0.75rem;     /* 12px */
```

### Typography Patterns
```css
/* Hero headline */
.hero h1 {
  font-size: var(--text-hero);
  font-weight: 800;
  letter-spacing: -0.02em;
  line-height: 1.1;
}

/* Section headers */
.section h2 {
  font-size: var(--text-display);
  font-weight: 700;
  letter-spacing: -0.01em;
}

/* Data/numbers (product app) */
.data-value {
  font-family: var(--font-mono);
  font-weight: 600;
  font-variant-numeric: tabular-nums;
}
```

---

## 3. SPACING SYSTEM

```css
/* 4px base unit */
--space-1: 0.25rem;   /* 4px */
--space-2: 0.5rem;    /* 8px */
--space-3: 0.75rem;   /* 12px */
--space-4: 1rem;      /* 16px */
--space-6: 1.5rem;    /* 24px */
--space-8: 2rem;      /* 32px */
--space-12: 3rem;     /* 48px */
--space-16: 4rem;     /* 64px */
--space-20: 5rem;     /* 80px */

/* Section padding */
.section {
  padding: var(--space-16) 0;
}

/* Container */
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 var(--space-4);
}
```

---

## 4. SHADOWS & ELEVATION

```css
/* Shadow system */
--shadow-sm: 0 1px 2px 0 rgb(0 0 0 / 0.3);
--shadow-md: 0 4px 6px -1px rgb(0 0 0 / 0.4), 0 2px 4px -2px rgb(0 0 0 / 0.3);
--shadow-lg: 0 10px 15px -3px rgb(0 0 0 / 0.5), 0 4px 6px -4px rgb(0 0 0 / 0.4);
--shadow-xl: 0 20px 25px -5px rgb(0 0 0 / 0.6), 0 8px 10px -6px rgb(0 0 0 / 0.5);

/* Glow effects */
--glow-primary: 0 0 20px rgba(14, 165, 233, 0.3);
--glow-secondary: 0 0 20px rgba(139, 92, 246, 0.3);
--glow-cta: 0 0 30px rgba(14, 165, 233, 0.4);

/* Card elevation */
.card {
  box-shadow: var(--shadow-md);
  transition: box-shadow 0.2s ease, transform 0.2s ease;
}

.card:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-2px);
}

/* Active/pressed state */
.card:active,
.button:active {
  transform: translateY(0);
  box-shadow: var(--shadow-sm);
}
```

---

## 5. CARDS & COMPONENTS

### Card Base
```css
.card {
  background: var(--bg-secondary);
  border: 1px solid var(--border-subtle);
  border-radius: 12px;
  padding: var(--space-6);
  box-shadow: var(--shadow-md);
  transition: all 0.2s ease;
}

.card:hover {
  border-color: var(--border-default);
  box-shadow: var(--shadow-lg);
  transform: translateY(-2px);
}

/* Glassmorphism variant */
.card-glass {
  background: rgba(17, 24, 39, 0.7);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.1);
}
```

### Buttons
```css
/* Primary CTA */
.btn-primary {
  background: linear-gradient(135deg, #0ea5e9 0%, #8b5cf6 100%);
  color: white;
  font-weight: 600;
  padding: var(--space-3) var(--space-6);
  border-radius: 8px;
  box-shadow: var(--glow-cta);
  transition: all 0.15s ease;
}

.btn-primary:hover {
  filter: brightness(1.1);
  box-shadow: 0 0 40px rgba(14, 165, 233, 0.5);
}

.btn-primary:active {
  transform: scale(0.98);
}

/* Secondary */
.btn-secondary {
  background: var(--bg-tertiary);
  color: var(--text-primary);
  border: 1px solid var(--border-default);
}

.btn-secondary:hover {
  background: var(--bg-elevated);
  border-color: var(--border-focus);
}

/* Ghost */
.btn-ghost {
  background: transparent;
  color: var(--text-secondary);
}

.btn-ghost:hover {
  color: var(--text-primary);
  background: var(--bg-tertiary);
}
```

### Status Indicators
```css
/* Status dot with pulse */
.status-dot {
  position: relative;
  width: 8px;
  height: 8px;
  border-radius: 50%;
}

.status-dot::before {
  content: '';
  position: absolute;
  inset: -4px;
  border-radius: 50%;
  animation: pulse 2s ease-in-out infinite;
}

.status-red { background: var(--status-red); }
.status-red::before { background: rgba(239, 68, 68, 0.4); }

.status-yellow { background: var(--status-yellow); }
.status-yellow::before { background: rgba(245, 158, 11, 0.4); }

.status-green { background: var(--status-green); }
.status-green::before { background: rgba(34, 197, 94, 0.4); }

@keyframes pulse {
  0%, 100% { transform: scale(1); opacity: 1; }
  50% { transform: scale(2); opacity: 0; }
}

/* Status badge */
.status-badge {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 4px 10px;
  border-radius: 9999px;
  font-size: var(--text-xs);
  font-weight: 500;
}

.status-badge-active {
  background: rgba(59, 130, 246, 0.15);
  color: #60a5fa;
  border: 1px solid rgba(59, 130, 246, 0.3);
}
```

---

## 6. ANIMATIONS

```css
/* Fade in up */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Shimmer for gradient text */
@keyframes shimmer {
  0% { background-position: 0% center; }
  100% { background-position: 200% center; }
}

/* Subtle float */
@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}

/* Spin for loading */
@keyframes spin {
  to { transform: rotate(360deg); }
}

/* Utility classes */
.animate-fade-in-up {
  animation: fadeInUp 0.5s ease-out forwards;
}

.animate-shimmer {
  background-size: 200% auto;
  animation: shimmer 8s linear infinite;
}

.animate-float {
  animation: float 6s ease-in-out infinite;
}

/* Stagger children */
.stagger-children > * {
  opacity: 0;
  animation: fadeInUp 0.4s ease-out forwards;
}

.stagger-children > *:nth-child(1) { animation-delay: 0.05s; }
.stagger-children > *:nth-child(2) { animation-delay: 0.1s; }
.stagger-children > *:nth-child(3) { animation-delay: 0.15s; }
.stagger-children > *:nth-child(4) { animation-delay: 0.2s; }
.stagger-children > *:nth-child(5) { animation-delay: 0.25s; }
```

---

## 7. BACKGROUND EFFECTS

```css
/* Noise texture overlay */
.noise-overlay::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
  z-index: 1000;
  opacity: 0.03;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)'/%3E%3C/svg%3E");
}

/* Grid pattern */
.grid-pattern {
  background-image: 
    linear-gradient(rgba(14, 165, 233, 0.03) 1px, transparent 1px),
    linear-gradient(90deg, rgba(14, 165, 233, 0.03) 1px, transparent 1px);
  background-size: 60px 60px;
}

/* Dot grid */
.dot-grid {
  background-image: radial-gradient(rgba(14, 165, 233, 0.15) 1px, transparent 1px);
  background-size: 24px 24px;
}

/* Radial glow */
.radial-glow {
  background: 
    radial-gradient(circle at 20% 50%, rgba(14, 165, 233, 0.08) 0%, transparent 50%),
    radial-gradient(circle at 80% 20%, rgba(139, 92, 246, 0.06) 0%, transparent 40%);
}
```

---

## 8. MARKETING SITE SPECIFIC

### Hero Section Structure
```html
<section class="hero aurora-bg">
  <div class="container">
    <!-- Trust bar -->
    <div class="trust-bar">
      <span class="stars">★★★★★</span>
      <span>Rated 4.9/5 by DSP owners</span>
    </div>
    
    <!-- Headline -->
    <h1 class="gradient-text animate-shimmer">
      Hours tracking that actually works for Amazon DSPs
    </h1>
    
    <!-- Subheadline -->
    <p class="subtitle">
      Built by a dispatcher. No bloat. No enterprise sales cycle. 
      Just the tools you need to stay compliant and save time.
    </p>
    
    <!-- CTAs -->
    <div class="cta-group">
      <a href="#" class="btn-primary">Start free trial</a>
      <a href="#" class="btn-ghost">Watch demo →</a>
    </div>
    
    <!-- Social proof -->
    <div class="social-proof">
      <p>Trusted by DSPs managing 10,000+ routes</p>
      <!-- Logo strip -->
    </div>
  </div>
</section>
```

### Feature Cards
```html
<div class="card feature-card">
  <div class="feature-icon">
    <!-- Icon -->
  </div>
  <h3>DOT Compliance Alerts</h3>
  <p>Automatic warnings when drivers approach 60/70 hour limits.</p>
  <a href="#" class="learn-more">Learn more →</a>
</div>
```

---

## 9. PRODUCT APP SPECIFIC

### Dashboard Stats
```tsx
<div className="grid grid-cols-2 sm:grid-cols-4 gap-3">
  {stats.map((stat, i) => (
    <button
      key={i}
      className="card stat-card"
      style={{
        boxShadow: isActive ? 'var(--glow-primary)' : 'var(--shadow-md)'
      }}
    >
      <span className="data-value text-2xl" style={{ color: stat.color }}>
        {stat.value}
      </span>
      <span className="text-xs text-gray-400">{stat.label}</span>
      {/* Mini progress bar */}
      <div className="w-full h-1 bg-gray-700 rounded-full mt-2 overflow-hidden">
        <div 
          className="h-full rounded-full transition-all duration-500"
          style={{ 
            width: `${stat.percent}%`,
            backgroundColor: stat.color 
          }}
        />
      </div>
    </button>
  ))}
</div>
```

### Driver Row
```tsx
<div className="card driver-row flex items-center gap-4 p-4">
  {/* Status with pulse */}
  <div className="status-dot status-green" />
  
  {/* Driver info */}
  <div className="flex-1 min-w-0">
    <h4 className="font-medium truncate">{driver.name}</h4>
    <p className="text-sm text-gray-400">{driver.station}</p>
  </div>
  
  {/* Hours with progress */}
  <div className="hidden sm:block w-24">
    <span className="data-value text-sm" style={{ color: hoursColor }}>
      {driver.hours}h
    </span>
    <div className="h-1 bg-gray-700 rounded-full mt-1 overflow-hidden">
      <div 
        className="h-full rounded-full"
        style={{ 
          width: `${Math.min((driver.hours / 50) * 100, 100)}%`,
          backgroundColor: hoursColor 
        }}
      />
    </div>
  </div>
  
  {/* Actions */}
  <div className="flex items-center gap-2">
    <button className="btn-primary text-sm px-4 py-2">
      Clock In
    </button>
  </div>
</div>
```

---

## 10. IMPLEMENTATION CHECKLIST

### Phase 1: Foundation (High Impact, Low Risk)
- [ ] Update color variables in CSS
- [ ] Add shadow system
- [ ] Update border radius to 12px on cards
- [ ] Add hover lift to cards

### Phase 2: Marketing Site Polish
- [ ] Add aurora background to hero
- [ ] Implement gradient text for H1
- [ ] Add noise texture overlay
- [ ] Update CTA buttons with glow
- [ ] Add stagger animations to feature cards

### Phase 3: Product App Polish
- [ ] Add elevation to stat cards
- [ ] Implement status dots with pulse
- [ ] Add progress bars to hours display
- [ ] Update buttons with micro-interactions
- [ ] Add loading animation improvements

### Phase 4: Advanced (Optional)
- [ ] Glassmorphism cards
- [ ] Parallax scroll effects
- [ ] Advanced page transitions
- [ ] Custom cursor effects

---

## 11. COMPETITOR INSIGHTS SUMMARY

| Competitor | Best Pattern | Steal This |
|------------|--------------|------------|
| **Samsara** | Navy + cyan enterprise palette | Trust-focused color strategy |
| **Deputy** | Bold purple gradient hero | Friendly, approachable vibe |
| **When I Work** | Clean green simplicity | Minimalist card design |
| **7shifts** | Orange energy | Strong CTAs and contrast |
| **Clockify** | Clean blue hierarchy | Clear information architecture |

**DSP Forge Differentiation:**
- Teal + violet palette (unique in space)
- Dispatcher-built authenticity
- No enterprise bloat messaging
- Mobile-first for field use
