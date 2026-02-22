# Workout Tracker — Spec

## Overview
Mobile-first workout tracker, deployed via GitHub Pages (chewyblooey/workout-tracker). Static HTML/CSS/JS, PWA-capable, no backend. Data in localStorage.

## Target User
Bryan — lifting 4-5x/week, tracking progressive overload, wants minimal friction mid-workout.

## Core Features

### 1. Quick Log
- Select exercise from pre-built list (tap, not type)
- Enter weight + reps per set (big buttons, thumb-friendly)
- Auto-fills last session's weight/reps as starting point
- Shows what to beat (last session's numbers)

### 2. Rest Timer
- Starts automatically when a set is logged
- Default 3 min (configurable per exercise)
- Big countdown display with progress bar
- Vibrates/beeps when done
- Tap to skip early

### 3. Workout Templates
- Pre-built routines (e.g. Push Day, Pull Day, Legs)
- Tap to start, walks through each exercise in order
- Add/edit exercises and templates easily

### 4. Progress Tracking
- Per-exercise history: weight x reps over time
- Simple line chart showing progression
- Auto-highlights PRs (personal records) 🎉

### 5. Today's View
- Open app → see today's workout
- Each exercise shows last session's numbers + target
- Check off sets as you go

## Design
- Single index.html — no frameworks
- Mobile-first, LIGHT MODE — beige/sandy background, black 8-bit text
- Pixel/monospace font, blocky progress bars, retro game aesthetic
- "LEVEL UP!" on PRs, streak counter, chiptune-style beep on timer end
- Big touch targets, minimal scrolling
- PWA manifest for "Add to Home Screen"
- LocalStorage for all data
- Export/import JSON option (backup)

## Layout Concept
```
┌─────────────────────────┐
│  🏋️ Push Day            │
│  Feb 20, 2026           │
├─────────────────────────┤
│  Bench Press            │
│  Last: 155 x 5,5,5      │
│                         │
│  Set 1: [155] x [5]  ✓ │
│  Set 2: [155] x [_]    │
│                         │
│  ⏱️  2:34 remaining     │
│  ████████░░░░  REST     │
│                         │
├─────────────────────────┤
│  Next: Incline DB Press │
└─────────────────────────┘
```

## Workout Split & Exercises

### Day 1: Chest / Shoulders
- Bench Press
- Chest Flys (cable or dumbbell)
- Decline Barbell Press
- Front Shoulder Raises
- Lateral Shoulder Raises
- *Added — Overhead Press (builds functional pressing strength + shoulders)*
- *Added — Face Pulls (rear delt health, balances all the pressing, injury prevention)*

### Day 2: Back / Biceps
- Lat Pulldowns
- Straight-Arm Pulldowns (standing, straight bar overhead, pull down with lats)
- Inverted Rows / Back Extension Raises (the one where you hang over the pad and lift yourself)
- Dumbbell Curls
- Barbell Curls
- *Added — Seated Cable Rows (thickness + posture, complements the pulldowns)*
- *Added — Hammer Curls (hits brachialis, makes arms look bigger from the side)*

### Day 3: Legs / Triceps
- TBD (Bryan to fill in)
- *Recommended:*
  - *Squats or Leg Press (quad dominant, foundational)*
  - *Romanian Deadlifts (hamstrings + glutes, huge for athleticism and injury prevention)*
  - *Walking Lunges (single-leg stability, athletic carryover)*
  - *Calf Raises (don't skip these)*
  - *Tricep Pushdowns (cable)*
  - *Overhead Tricep Extension (long head, fills out the arm)*
  - *Close-Grip Bench or Dips (compounds for triceps)*

### Recommendations for Functional Strength / Injury Prevention
- **Core work 2x/week**: Planks, hanging leg raises, cable woodchops — protects your back, improves everything
- **Deadlifts or RDLs**: The single best exercise for posterior chain (back, glutes, hamstrings) — keeps you athletic and injury-resistant
- **Farmer's Carries**: Grip, core, traps, conditioning — 2-3 sets at end of any session, just grab heavy dumbbells and walk
- **Face Pulls**: Rear delts + rotator cuff health — critical with all the pressing you're doing

## Bryan's Current Stats (for default templates)
- Bench: 135x15, 145x10, 155x6-8, 165x3 (max)
- Rest between sets: 3 min (heavy), adjust for accessories
- Goal: progressive overload tracking, hit 165+ bench

## Deployment
- Repo: chewyblooey/workout-tracker (GitHub Pages)
- Same workflow as kanban board

## R1 QA Notes (RESOLVED)
- ✅ Rest timer runs slow when navigating away — fixed: wall-clock based timer
- ✅ Add ability to remove/delete individual sets — fixed: ✕ button per set

## Backlog

## Nice-to-Haves (v2)
- Weekly volume summary
- Body weight log
- Export to CSV
- Share workout with someone
- Calorie/protein quick log
- Superset/circuit timer mode

## Roadmap — Native iOS App (v3)
Status: Future — needs Apple Developer account + Xcode confirmed
- Rebuild as native SwiftUI iOS app
- WatchOS companion app (log sets from wrist, rest timer on Watch)
- HealthKit integration (read heart rate, calories, workout sessions, sleep, VO2 max from Apple Watch)
- Correlate data: sleep quality vs performance, heart rate during sets, recovery trends
- MyFitnessPal API integration (nutrition/macros/protein tracking — all-in-one view)
- Prerequisites: Apple Developer account ($99/yr), Xcode on Bryan's Mac

## Bench Press Program (4 weeks)
Built to break through 165 plateau:

### Day 1 — Heavy Day
- 135 x 8 (warmup)
- 145 x 5
- 155 x 5
- 155 x 5
- 155 x 5

### Day 2 — Volume Day
- 135 x 10
- 140 x 8
- 140 x 8
- 140 x 8

### Weekly Progression
- Weeks 1-2: As written
- Week 3: Heavy day → 160x4x3, Volume day → 145x8x3
- Week 4: Test week — 135x5, 145x3, 155x2, 165x1, attempt 170

## Fitness Notes
- Protein: 0.8-1g per lb current bodyweight, every day (training + rest)
- Rest days: protein stays same, calories can be slightly lower (200-300 cal)
- Goal: recomp — lose fat, gain muscle, target weight lower but more muscular
- Alcohol: avoid on training days, blunts protein synthesis 20-30%
- Soreness ≠ growth indicator — track lifts instead
