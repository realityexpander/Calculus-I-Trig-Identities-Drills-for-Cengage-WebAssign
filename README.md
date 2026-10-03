# Calculus I Identities & Rules Drill

A single-page browser app for memorizing and practicing trigonometric identities and Calculus I derivative rules through active recall.

The app does **not** use multiple-choice questions. It shows one side of an equation and requires the user to type the missing side using an interactive mathematical equation editor.

## Features

- Written-answer practice using a real equation editor
- LaTeX-rendered mathematical expressions
- Math input provided by [MathLive](https://mathlive.io/)
- Symbolic parsing/checking with the [CortexJS Compute Engine](https://cortexjs.io/compute-engine/)
- Drill a single section or all sections
- Drill left-to-right, right-to-left, or both directions randomly
- Randomized questions
- Avoids immediate question repetition when possible
- **Check Answer**, **Reveal**, and **Next Identity** controls
- macOS Option-key and Windows Alt-key shortcuts
- Reveal-to-Enter workflow for quickly advancing
- Session statistics for Completed, Correct, Percentage correct, and Current streak
- Reset Score control
- Responsive desktop/mobile layout
- Single-file HTML app

## Sections

### 1. Reciprocal Identities

$$
\csc x=\frac{1}{\sin x}
$$

$$
\sec x=\frac{1}{\cos x}
$$

$$
\cot x=\frac{1}{\tan x}
$$

### 2. Quotient Identities

$$
\tan x=\frac{\sin x}{\cos x}
$$

$$
\cot x=\frac{\cos x}{\sin x}
$$

### 3. Pythagorean Identities

$$
\sin^2x+\cos^2x=1
$$

$$
1+\tan^2x=\sec^2x
$$

$$
1+\cot^2x=\csc^2x
$$

### 4. Useful Rearrangements

Includes forms such as:

$$
1-\sin^2x=\cos^2x
$$

$$
\sec^2x-1=\tan^2x
$$

$$
1-\sec^2x=-\tan^2x
$$

### 5. Even / Odd Identities

Examples:

$$
\sin(-x)=-\sin x
$$

$$
\cos(-x)=\cos x
$$

$$
\tan(-x)=-\tan x
$$

### 6. Double-Angle Identities

Includes:

$$
\sin(2x)=2\sin x\cos x
$$

$$
\cos(2x)=\cos^2x-\sin^2x
$$

$$
\tan(2x)=\frac{2\tan x}{1-\tan^2x}
$$

### 7. Power-Reduction / Half-Angle Forms

$$
\sin^2x=\frac{1-\cos(2x)}{2}
$$

$$
\cos^2x=\frac{1+\cos(2x)}{2}
$$

### 8. Sum and Difference Identities

Includes sine, cosine, and tangent sum/difference formulas.

### 9. Cofunction Identities

Examples:

$$
\sin\left(\frac{\pi}{2}-x\right)=\cos x
$$

$$
\cos\left(\frac{\pi}{2}-x\right)=\sin x
$$

### 10. Core Seven — Highest Priority Review

Focused review of:

$$
\tan x=\frac{\sin x}{\cos x}
$$

$$
\cot x=\frac{\cos x}{\sin x}
$$

$$
\sec x=\frac{1}{\cos x}
$$

$$
\csc x=\frac{1}{\sin x}
$$

$$
\sin^2x+\cos^2x=1
$$

$$
1+\tan^2x=\sec^2x
$$

$$
1+\cot^2x=\csc^2x
$$

### 11. Calculus I Derivative Rules

This section includes:

- Constant rule
- Identity rule
- Constant multiple rule
- Sum and difference rules
- Power rule
- General power rule
- Product rule
- Quotient rule
- Chain rule
- \(1/x\) rule
- Square-root derivative
- Exponential rules
- Natural-log and general logarithm rules
- Composite exponential/logarithmic rules
- All six basic trigonometric derivatives
- All six inverse-trigonometric derivatives
- Inverse-function derivative rule
- Implicit differentiation notation
- General logarithmic-differentiation form for \(u^v\)

Examples:

$$
\frac{d}{dx}[x^n]=nx^{n-1}
$$

$$
\frac{d}{dx}[uv]=u'v+uv'
$$

$$
\frac{d}{dx}\left[\frac{u}{v}\right]
=
\frac{vu'-uv'}{v^2}
$$

$$
\frac{d}{dx}[f(g(x))]
=
f'(g(x))g'(x)
$$

$$
\frac{d}{dx}[\sin x]=\cos x
$$

$$
\frac{d}{dx}[\arctan x]
=
\frac{1}{1+x^2}
$$

## Keyboard Shortcuts

### Reveal

On macOS:

```text
Option-R
```

The button displays:

```text
Reveal ⌥R
```

On Windows and other non-Mac platforms:

```text
Alt-R
```

The button displays:

```text
Reveal alt-R
```

### Next Identity

On macOS:

```text
Option-N
```

The button displays:

```text
Next Identity ⌥N
```

On Windows and other non-Mac platforms:

```text
Alt-N
```

The button displays:

```text
Next Identity alt-N
```

The app uses `KeyboardEvent.code` with `KeyR` and `KeyN`, together with the Alt/Option modifier. This allows the shortcut to work on macOS even when Option-key combinations would otherwise type special characters.

## Reveal → Enter Workflow

After **Reveal** is selected:

1. The correct answer is shown.
2. **Next Identity** becomes the highlighted action.
3. Keyboard focus moves to **Next Identity**.
4. Pressing **Enter** advances immediately to the next question.

When the next question loads, the highlighted action resets to **Check Answer**.

## Answer Entry

Each question displays one side of an equation and leaves the other side blank.

Example:

$$
\tan x=\boxed{\phantom{\frac{\sin x}{\cos x}}}
$$

The user enters:

$$
\frac{\sin x}{\cos x}
$$

The direction may also be reversed:

$$
\boxed{\phantom{\tan x}}=\frac{\sin x}{\cos x}
$$

## Answer Checking

The app first attempts symbolic comparison using the CortexJS Compute Engine.

If symbolic comparison cannot confirm an answer, it falls back to normalized LaTeX comparison.

Because the program is intended as a memorization drill, the expected answer is the identity or rule form being practiced.

## Statistics

| Statistic | Description |
|---|---|
| **Completed** | Number answered correctly or revealed |
| **Correct** | Number answered correctly without Reveal |
| **Percentage correct** | `Correct ÷ Completed × 100`, rounded to the nearest whole percent |
| **Current streak** | Consecutive correct answers |

A revealed answer counts as completed but not correct.

**Reset Score** clears all four statistics.

Statistics are session-only and are not currently saved after the page is reloaded or the browser is closed.

## Identity Equation Sheet

The app links to the companion reference sheet:

[Identity Equation Sheet PDF](https://realityexpander.github.io/Calculus-I-Trig-Identities-Drills-for-Cengage-WebAssign/trig_identities_cheat_sheet.pdf)

## Running the App

No installation or build process is required.

1. Download or clone the repository.
2. Open the HTML file in a modern browser.
3. Select an identity/rule section.
4. Select a drill direction.
5. Type the missing mathematical expression.
6. Use **Check Answer**, **Reveal**, or the keyboard shortcuts.

## Internet Requirement

The application itself is contained in one HTML file, but MathLive and the CortexJS Compute Engine are loaded from a CDN. An internet connection is therefore required when the page starts.

## Technology

- HTML5
- CSS
- JavaScript ES modules
- [MathLive](https://github.com/arnog/mathlive)
- [CortexJS Compute Engine](https://github.com/cortex-js/compute-engine)

MathLive and CortexJS Compute Engine are open-source projects distributed under the MIT License.

## Project Structure

```text
.
├── Calculus_I_trig_identity_drill_v3.html
├── trig_identities_cheat_sheet.pdf
└── README.md
```

If the GitHub Pages deployment uses `index.html`, rename or copy the current versioned HTML file to `index.html` when publishing.

## Browser Compatibility

A current version of Safari, Chrome, Firefox, Edge, or another Chromium-based browser is recommended. JavaScript must be enabled.

## Source Code

[GitHub — Calculus-I-Trig-Identities-Drills-for-Cengage-WebAssign](https://github.com/realityexpander/Calculus-I-Trig-Identities-Drills-for-Cengage-WebAssign)

## Copyright

©2026 Chris Athanas

## Disclaimer

This is an independent educational study tool and is not affiliated with or endorsed by Texas Instruments, Cengage, Larson Calculus, or the publishers of any referenced textbook or homework system.
