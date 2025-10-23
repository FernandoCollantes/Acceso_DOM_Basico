# AI Agent Instructions for Acceso_DOM_Basico

## Project Overview
This is a basic DOM manipulation learning project that demonstrates various ways to access and modify HTML elements using JavaScript. The project is structured as a single HTML file with embedded JavaScript code showcasing different DOM manipulation techniques.

## Project Structure
- Root file: `index.html` - Contains both HTML structure and JavaScript code
- Dependencies: Bootstrap 5.3.3 (loaded via CDN)

## Key Components and Patterns

### DOM Selection Methods
The project demonstrates multiple DOM selection approaches:
1. `getElementById()` - Used for single element selection by ID
2. `getElementsByTagName()` - For collecting elements by tag name (returns live HTMLCollection)
3. `getElementsByClassName()` - For selecting elements by class (returns live HTMLCollection)
4. `querySelector()` - For selecting first matching element using CSS selectors
5. `querySelectorAll()` - For selecting all matching elements (returns static NodeList)

### Element Creation Pattern
When creating new elements dynamically, follow this pattern:
```javascript
const element = document.createElement("tag");
element.className = "class-name";
element.textContent = "content";
parentElement.appendChild(element);
```

### Collection Handling
- For `querySelectorAll()` results, use `forEach()` for iteration
- For `getElementsBy*` methods, use traditional `for` loops as they return HTMLCollections

### Styling Convention
Direct style modifications are done using the `style` property:
```javascript
element.style.propertyName = "value";
```

## Development Workflow
1. The project runs directly in a web browser through XAMPP's htdocs directory
2. No build process required
3. Access via `http://localhost/Acceso_DOM_Basico/`

## Best Practices
1. Always check if elements exist before manipulating them
2. Use appropriate selector methods based on the use case:
   - Single element by ID: `getElementById()`
   - Dynamic collections: `getElementsBy*` methods
   - Static collections: `querySelectorAll()`
3. Group related DOM manipulations together in the code

## Project Boundaries
- Single page application with inline JavaScript
- No external JavaScript files
- Bootstrap is the only external dependency