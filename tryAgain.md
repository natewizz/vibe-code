# LLM Instructions: Debugging Persistent Issues for Basic Vibe Coders

**When quick fixes haven't worked and the problem persists, follow this systematic debugging approach to get to the root cause.**

---

## 0 · Issue Assessment & Context Building

Before diving deep, establish the full picture:

1. **Problem definition** - What exactly is broken? What should happen vs. what actually happens?
2. **Reproduction steps** - Can you consistently trigger the issue?
3. **Recent changes** - What was modified in the last day/week that might be related?
4. **Environment details** - Browser, device, network conditions, data conditions
5. **Error manifestation** - Console errors, visual bugs, performance issues, silent failures?
6. **Impact scope** - Is it affecting one feature, multiple features, or the entire app?

**Always reproduce the issue yourself before attempting fixes.**

---

## 1 · Evidence Gathering & Documentation

### Browser Investigation
- **Console errors** - All errors, warnings, and logs
- **Network tab** - Failed requests, slow responses, malformed data
- **Elements inspector** - DOM structure, computed styles, event listeners
- **Application tab** - Local storage, session storage, cookies, service workers
- **Performance tab** - Memory leaks, slow renders, blocking scripts

### Code Investigation
- **Recent git history** - What commits happened around when issue started?
- **Dependency changes** - Package.json modifications, lock file changes
- **Configuration drift** - Environment variables, build settings, deployment configs
- **Data structure changes** - API responses, database schema, file formats

### System Investigation
- **Development environment** - Node version, npm/yarn version, OS differences
- **Build process** - Are build errors being masked? Development vs production differences
- **External dependencies** - Third-party API issues, CDN problems, service outages

---

## 2 · Root Cause Investigation

### Systematic Elimination
1. **Isolate the problem** - Narrow down to smallest possible reproduction case
2. **Test assumptions** - Verify each piece of the data/logic chain
3. **Bisect the changes** - Use git bisect or manual rollback to find breaking change
4. **Compare environments** - Does it work in different browsers/devices/accounts?
5. **Strip complexity** - Remove non-essential code to isolate core issue

### Common Root Cause Categories
- **Timing issues** - Race conditions, async/await problems, load order dependencies
- **State management** - Stale closures, incorrect state updates, state synchronization
- **Data flow problems** - Incorrect API responses, data transformation errors, caching issues
- **Environment differences** - Development vs production, browser inconsistencies
- **Dependency conflicts** - Version mismatches, breaking changes, peer dependency issues
- **Configuration errors** - Missing environment variables, incorrect build settings

### Deep Dive Techniques
- **Add extensive logging** - Trace data flow through entire system
- **Use debugger breakpoints** - Step through code execution line by line
- **Mock/stub dependencies** - Isolate whether problem is internal or external
- **Test with different data** - Edge cases, empty data, malformed data, large datasets
- **Performance profiling** - Memory usage, render times, network waterfall

---

## 3 · Hypothesis Formation & Testing

### Generate Multiple Hypotheses
1. **Most likely cause** - Based on symptoms and recent changes
2. **Alternative explanations** - What else could cause these symptoms?
3. **Edge case scenarios** - Unusual data/user behavior that might trigger issue
4. **Environmental factors** - Browser quirks, network conditions, device limitations

### Test Each Hypothesis
- **Create minimal test case** - Smallest possible code that demonstrates the issue
- **Modify one variable at a time** - Systematic testing to isolate cause
- **Document test results** - What worked, what didn't, what was inconclusive
- **Verify fixes don't break other things** - Regression testing after each change

### Data-Driven Debugging
- **Log everything relevant** - Input data, intermediate values, output data
- **Compare working vs broken states** - What's different between them?
- **Test boundary conditions** - Empty data, null values, maximum limits
- **Verify assumptions about data structure** - Is the API returning what you expect?

---

## 4 · Solution Strategy & Implementation

### Fix Categories
- **Quick fix** - Patch the immediate symptom to unblock user
- **Root cause fix** - Address the underlying problem properly
- **Preventive measures** - Add safeguards to prevent similar issues

### Implementation Approach
1. **Create backup/branch** - Save current state before making changes
2. **Implement minimal fix first** - Get it working with simplest possible solution
3. **Test thoroughly** - Verify fix works in all scenarios that were failing
4. **Improve the solution** - Make it more robust, readable, maintainable
5. **Add prevention** - Error handling, validation, testing to prevent recurrence

### Complex Issue Patterns

#### State Synchronization Issues
1. Check for stale state references
2. Verify state update timing and dependencies
3. Add state debugging tools/logging
4. Consider using useCallback/useMemo for optimization
5. Test with React DevTools for state changes

#### API Integration Problems
1. Verify API contract hasn't changed
2. Check request/response formats and headers
3. Test with different data scenarios
4. Add proper error handling and retries
5. Monitor network tab for failed/slow requests

#### Performance Degradation
1. Profile memory usage and identify leaks
2. Analyze bundle size and code splitting
3. Check for unnecessary re-renders
4. Optimize database queries or API calls
5. Add performance monitoring and alerting

---

## 5 · Verification & Regression Prevention

### Comprehensive Testing
- **Original issue resolved** - Problem no longer occurs in any scenario
- **No new issues introduced** - Existing functionality still works
- **Edge cases handled** - Solution works with unusual data/scenarios
- **Performance impact acceptable** - No significant slowdowns introduced
- **Cross-browser compatibility** - Works in all target browsers

### Documentation & Prevention
- **Document the issue** - What was the problem and how was it solved?
- **Add tests if applicable** - Prevent regression of this specific issue
- **Update error handling** - Better error messages for similar future issues
- **Improve monitoring** - Add logging/alerts to catch similar issues early
- **Share knowledge** - Update team/documentation with lessons learned

### Future-Proofing
- **Review related code** - Are there similar patterns that might have same issue?
- **Update development practices** - How can we prevent this category of issue?
- **Improve debugging tools** - What would have made this faster to diagnose?
- **Consider architecture changes** - Does this reveal a deeper design problem?

---

## 6 · Escalation & External Help

### When to Ask for Help
- **After 4+ hours of systematic debugging** - Don't waste entire days
- **Security implications** - Authentication, data exposure, injection attacks
- **Performance issues affecting users** - Site slowdowns, crashes, memory issues
- **Complex architecture decisions** - Database design, API architecture, state management
- **Third-party service integration** - Payment processing, external APIs, cloud services

### Information to Provide
- **Complete problem description** - Symptoms, reproduction steps, expected behavior
- **Debugging evidence** - Console logs, network traces, error messages
- **Code samples** - Minimal reproduction case and relevant code sections
- **Environment details** - Versions, browser, deployment environment
- **What you've tried** - All attempted solutions and their results

---

## 7 · Success Criteria

A successful deep debugging session should result in:
- ✅ **Issue completely resolved** - Problem no longer occurs in any scenario
- ✅ **Root cause identified** - Understanding of why it happened
- ✅ **Solution is robust** - Handles edge cases and prevents recurrence
- ✅ **No regressions introduced** - Existing functionality remains intact
- ✅ **Knowledge captured** - Documentation/tests prevent similar future issues

**Goal: Not just fix the symptom, but understand and prevent the underlying problem.**