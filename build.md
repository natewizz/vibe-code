# LLM Instructions: Building Features for Basic Vibe Coders

**When user requests a specific feature, follow this systematic approach to build it efficiently with minimal back-and-forth.**

---

## 0 · Feature Request Analysis

Before writing any code, extract these specifics:

1. **Core functionality** - What exactly should this feature do?
2. **Data requirements** - What data does it need? Where does that data come from?
3. **UI placement** - Where in the app should this appear?
4. **User interaction** - Click, hover, form input, real-time updates?
5. **Integration points** - What existing components/APIs will this touch?

**Always restate the feature in clear terms before proceeding.**

---

## 1 · Codebase Assessment

### Rapid Context Gathering
- **Check existing patterns** - How are similar features implemented?
- **Identify component structure** - Where do new components typically go?
- **Review data flow** - How does data move through the app?
- **Find styling approach** - CSS modules, styled-components, plain CSS?
- **Check state management** - useState, Context, external store?

### Key Files to Examine
1. **Main app structure** - App.js, index.js, routing setup
2. **Similar existing features** - Components that do something similar
3. **Data layer** - API calls, data fetching, state management
4. **Styling system** - How styles are organized and applied
5. **Utility functions** - Shared helpers, constants, formatting

### Technology Stack Detection
- **Frontend framework** - React, Vue, vanilla JS, etc.
- **Build tool** - Vite, Create React App, Next.js, etc.
- **Styling solution** - CSS, Sass, styled-components, Tailwind
- **State management** - Local state, Context, Redux, Zustand
- **Data fetching** - fetch, axios, SWR, React Query

---

## 2 · Implementation Planning

### Feature Breakdown
1. **Data layer** - What data needs to be fetched/calculated?
2. **Component structure** - What components need to be created/modified?
3. **Styling needs** - New styles, responsive considerations
4. **Integration points** - How does this connect to existing features?
5. **Edge cases** - Loading states, error handling, empty data

### File Impact Assessment
- **New files needed** - Components, utilities, styles
- **Existing files to modify** - Parent components, routes, styles
- **Configuration changes** - Package.json dependencies, environment variables
- **Testing requirements** - What needs to be manually tested?

### Implementation Sequence
1. **Data foundation** - Get the data working first
2. **Basic component** - Minimal working version
3. **Integration** - Connect to existing app structure
4. **Styling** - Make it look good and responsive
5. **Polish** - Error handling, loading states, edge cases

---

## 3 · Execution Strategy

### Start with Data
- **Identify data source** - API endpoint, local calculation, existing state
- **Create data fetching logic** - Custom hook, service function, or direct API call
- **Test data flow** - Console.log to verify data structure and content
- **Handle loading/error states** - Basic error boundaries and loading indicators

### Build Component Foundation
- **Create minimal working component** - Just render the data, no styling
- **Use existing patterns** - Match how other components are structured
- **Add to parent component** - Import and render in the correct location
- **Verify basic functionality** - Does it appear and show data?

### Style and Polish
- **Match existing design** - Use the same patterns, colors, spacing
- **Add responsive behavior** - Test on different screen sizes
- **Implement interactions** - Hover states, click handlers, animations
- **Test edge cases** - Empty data, loading states, error conditions

---

## 4 · Common Feature Patterns

### Adding Charts/Visualizations
1. Check if charting library exists (Chart.js, D3, Recharts)
2. Install appropriate library if needed
3. Create reusable chart component
4. Format data for chart requirements
5. Add responsive behavior and loading states

### Adding Forms
1. Identify form library or use native HTML
2. Create controlled inputs with proper validation
3. Handle form submission and API calls
4. Add loading states and error handling
5. Integrate with existing data flow

### Adding API Integration
1. Check existing API patterns and utilities
2. Create or extend API service functions
3. Add proper error handling and retries
4. Implement loading states in UI
5. Update local state/cache appropriately

### Adding Real-time Features
1. Check if WebSocket/EventSource exists
2. Set up real-time connection if needed
3. Handle connection states and reconnection
4. Update UI reactively to data changes
5. Add proper cleanup on component unmount

---

## 5 · Quality Assurance

### Functional Testing
- **Primary feature works** - Core functionality operates as expected
- **Data accuracy** - Displayed data matches expected values
- **User interactions** - All buttons, links, forms work properly
- **Responsive design** - Works on mobile, tablet, desktop
- **Error scenarios** - Handles missing data, API failures gracefully

### Integration Testing
- **Doesn't break existing features** - Other parts of app still work
- **Proper styling integration** - Matches existing design system
- **Performance impact** - No significant slowdowns introduced
- **Browser compatibility** - Works in major browsers

### Code Quality Checks
- **Follows existing patterns** - Consistent with codebase conventions
- **Proper imports/exports** - All dependencies properly declared
- **No console errors** - Clean browser console
- **Clean code structure** - Readable, properly named variables/functions

---

## 6 · Delivery and Documentation

### Code Delivery
- **Provide complete implementation** - All necessary files and changes
- **Include installation steps** - Any new dependencies or setup required
- **Show exact file locations** - Where to place new files
- **Highlight key changes** - What was modified in existing files

### User Guidance
- **How to test the feature** - Specific steps to verify it works
- **How to customize** - Common modifications they might want
- **Troubleshooting** - Common issues and solutions
- **Next steps** - Logical extensions or improvements

### Documentation Updates
- **Update README if needed** - New dependencies, features, or setup steps
- **Comment complex logic** - Explain non-obvious code decisions
- **Environment variables** - Document any new config requirements
- **API documentation** - If new endpoints were created

---

## 7 · Success Criteria

A successful feature implementation should:
- ✅ **Works immediately** - User can copy/paste and see it working
- ✅ **Matches request** - Delivers exactly what was asked for
- ✅ **Integrates cleanly** - Fits naturally into existing app
- ✅ **Handles edge cases** - Graceful error handling and loading states
- ✅ **Follows patterns** - Consistent with existing codebase style

**Goal: Feature is complete, tested, and ready for real use.**
