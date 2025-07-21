# Contextify Demo Example: Company IntelliHub

**A realistic project example for demonstrating the Contextify tool with comprehensive, engaging descriptions.**

---

## Project Details

### Project Name
**IntelliHub - The Company Brain**

### Your Name
**Alex Chen**

### The Vision
I want to build the ultimate company intelligence dashboard that becomes every team's secret weapon. Think of it as a smart command center that pulls together all the scattered information floating around our company - from Slack conversations and GitHub commits to Google Drive documents and Jira tickets - and presents it in one beautiful, searchable interface. Instead of hunting through 47 different tools to find that one document or figure out who's working on what, everyone just opens IntelliHub and finds everything instantly.

### Keywords
company-intelligence, dashboard, data-aggregation, slack-integration, github-api, google-workspace, search-platform, team-productivity

---

## Project Context

### Project Description
Our company is drowning in information spread across dozens of tools. Sales updates live in Slack, code changes are buried in GitHub, important documents hide in Google Drive, project status updates scatter across Jira and Linear, and meeting notes vanish into Notion. When someone asks "What's the status on the Peterson project?" or "Who worked on the authentication system last month?", we waste 20 minutes playing digital archaeology.

IntelliHub solves this by creating a unified search and discovery platform that connects to all our existing tools without disrupting anyone's workflow. It's like having a super-smart assistant that knows everything happening in the company and can surface the right information at the right time. Users can search for projects, people, topics, or timeframes and get intelligent results that show the full context - not just individual files or messages.

### Development Constraints
- Must work with our existing Google Workspace, Slack, and GitHub setup
- Cannot store sensitive data permanently (privacy compliance)
- Should work on mobile devices for remote team members
- Budget-conscious - prefer free/open-source solutions where possible
- Small team of 3 developers, so avoid over-complex architectures
- Need to ship MVP within 6 weeks to prove value
- Must handle our team size of 50-75 people without performance issues

### Target Users
Primary: Project managers, team leads, and senior developers who need to track cross-team initiatives

Secondary: Sales team looking for technical context on customer conversations, new hires trying to understand company knowledge, executives wanting high-level visibility into what's happening

---

## Requirements & Examples

### Core Requirements
- **Universal Search**: Search across Slack messages, GitHub repos, Google Drive files, and Jira tickets from one interface
- **Smart Context**: When showing a GitHub commit, also show related Slack discussions and documentation
- **People Discovery**: Find out who worked on what, when, and with whom
- **Project Timeline Views**: See the evolution of projects across all platforms
- **Real-time Updates**: New information appears without manual refreshes
- **Permission Awareness**: Only show information users have access to in source systems
- **Mobile Responsive**: Works well on phones for remote team members
- **Fast Search**: Results appear within 2-3 seconds maximum

### Reference Examples
Think Linear's search experience but for everything company-wide, not just tasks. Similar to how Notion's search works across pages, but extended to external tools. The visual design should feel like Raycast or Spotlight - clean, fast, and focused on getting you to information quickly. For the dashboard view, inspiration from GitHub's insights page showing activity over time, but aggregated across all our tools.

### User Flow
User opens IntelliHub → sees dashboard with recent activity across all connected tools → types search query like "Peterson project authentication" → gets results showing related GitHub commits, Slack conversations, Google docs, and Jira tickets all ranked by relevance → clicks on any result to see full context plus related items → can save interesting searches or follow specific projects for updates

---

## Keep in Mind

### Don't Do This
- Don't build another chat tool or try to replace existing tools
- Avoid storing copies of sensitive data - use search indexes and references instead
- Don't create complex user management - leverage existing company SSO
- No blockchain, AI agents, or other buzzword-driven features that don't solve real problems
- Don't try to build custom integrations for every tool - focus on the big 4-5 that matter most
- Avoid real-time collaboration features - this is about discovery, not creation

### Success Looks Like
Team members stop asking "where did I see that thing about..." in Slack channels. Project managers can quickly generate status updates by searching for project names. New hires can explore company knowledge and understand project history. Average time to find company information drops from 15+ minutes to under 2 minutes. At least 60% of the team uses it weekly within the first month.

### If Stuck
Focus on search-first approach - perfect the search experience for just Slack and GitHub before adding more integrations. If API rate limits become an issue, implement smart caching and batch requests. If permissions get complex, start with a simple "trusted team" approach and add granular permissions later. Consider using existing search solutions like Elasticsearch or Algolia instead of building from scratch.

---

## What You Want

### AI Persona
You're a senior full-stack developer who has built several successful internal tools and data integration platforms. You understand API design, search systems, and the challenges of connecting multiple third-party services. You're practical about MVP development and know how to balance technical debt with shipping quickly. You've worked with teams of similar size and understand the productivity challenges that come with tool sprawl.

### The Ask
Help me architect and build IntelliHub as a modern web application that elegantly solves company information discovery. I need guidance on the technical approach - should this be a React frontend with Node.js backend, or would something like Next.js work better? What's the best way to handle authentication across multiple APIs? How should I structure the search indexing to be fast but not overwhelm third-party rate limits? 

I want specific recommendations for the technology stack, database choices for search indexing, and a development roadmap that gets me to a working MVP quickly. Also help me think through the API integration strategy - which services to connect first, how to handle different data types, and what the search ranking algorithm should prioritize.

Most importantly, I want this to feel fast and magical for users, not like another boring enterprise tool. How do I build something that people actually want to use?
