# Product Requirement Document (PRD): RoundRobinPro

## Overview
RoundRobinPro is a Software as a Service (SAAS) platform designed to help pickleball enthusiasts, organizers, and clubs create, manage, and optimize round robin events for any number of courts and players. The platform supports both doubles and singles play, offers advanced scheduling algorithms to minimize repeat matchups, and provides robust event and player management features. The application will be mobile-friendly (PWA), support user authentication (including social logins), and offer both free (ad-supported) and premium (ad-free, feature-rich) tiers.

## Target Users
- Individual players
- Event organizers
- Club administrators

## Core Features

### 1. User Management
- Multiple user roles: player, organizer, admin, club admin
- User authentication (email/password and social logins: Google)
- Player profiles, including optional DUPR or regional classification integration
- Import player lists (CSV, etc.)
- (TBD: Export player lists)
- Players can be in multiple groups; group names must be unique system-wide
- Direct messaging between players in the same group
- Easy onboarding via group code or invite link

### 2. Event & Calendar Management
- Users can create and manage multiple events
- Calendar view for upcoming, past, and recurring events
- Support for both singles and doubles event types
- Clubs/organizations can manage events for their members
- Events are private by default
- Event templates for common group/court sizes (e.g., 8/2, 12/3, 16/4)
- Event types: league, ladder, lesson, social, round robin
- RSVP/availability polling for events
- Photo sharing for event recaps
- .ics calendar file sent with participation confirmation emails

### 3. Scheduling Algorithm
- Optimized round robin scheduling for multiples of 4 (e.g., 8, 12, 16 players)
- Separate handling for singles and doubles events
- For non-multiples of 4 (e.g., 10 players, 3 courts: 2 doubles, 1 singles), flexible court assignment
- Minimize repeat teammates and opponents as much as possible
- Configurable session length, game duration, and number of games
- Manual overrides for schedule (organizer can swap players)
- Waitlist and substitute player support; notify subs if someone cancels

### 4. Notifications & Communication
- Email and SMS notifications (Twilio integration)
- Users can opt in/out of notification types and customize triggers
- Admins receive all notifications
- Event updates, reminders, and group communications
- Group chat for each event
- Direct messaging between players in the same group

### 5. Printing & Visuals
- Downloadable PDF schedule for printing (8.5x11 format) using a Vercel-compatible library
- Print-friendly web page option
- Initial version: simple table layout (court numbers optional, game times, player names in each cell)
- QR code on printout for online schedule access
- Future: graphical court layout (pickleball court graphic with player names)

### 6. Payments & Monetization
- Free tier (ad-supported, Google AdSense to start)
- Premium tier (ad-free, additional features)
- Stripe integration for payments
- Paid features: event creation, saving documents, recurring events, player history

### 7. Club/Organization Support
- Data model supports clubs/organizations from the start
- Club admins can manage members, events, and communications
- Option to print schedules with player names (not just numbers)
- Clubs can have branding (logo, colors) on schedules and event pages
- Club directory/search feature ("near me")
- Advanced admin tools: reporting, member management, communication tools

### 8. Player Management & Stats
- Player profiles with optional DUPR/regional classification
- Track participation history (premium feature)
- (TBD: stats, rankings)
- Privacy controls for profiles (e.g., hide from non-members)
- Enhanced privacy and safety features, especially for youth/public groups

### 9. Group Home/Landing Page
- Each group has a home/landing page accessible to members (requires login)
- Displays group name, admin(s) name(s), and participant photos
- Web-based display of group conversations (chat/messages)
- Gallery of photos shared by participants

### 10. Platform & Tech
- Mobile-friendly PWA from the start
- Built with Next.js, Tailwind CSS, shadcn/ui
- Supabase for backend/auth, storage, and real-time features
- Prisma for database/schema management
- Hosted on Vercel
- Offline access to schedules (PWA)
- Testing integrated into the development process (unit, integration, and E2E tests)

### 11. Technical Architecture
- Supabase used for authentication, database, file storage (photos, PDFs), and real-time features (chat, notifications, RSVP updates)
- PDF generation uses a Vercel-compatible library (e.g., @react-pdf/renderer or similar)
- .ics calendar file generation and email integration for event participation confirmations
- Two levels of admin dashboards:
  - Group Admin: manage group, events, members, and communications
  - Superadmin (SaaS owner): manage all groups, view platform analytics, revenue dashboard, and theme editor
- Scalable architecture with option to break out services as needed

### 12. UI/UX & Design
- Exceptional, modern UI/UX design principles
- Themeable design: all colors, typography, and component styles defined in a single theme file
- Light and dark mode (day/night themes)
- Consistent use of buttons, cards, and drop shadows throughout the site
- Accessibility (a11y) at a basic level (WCAG compliance, keyboard navigation, color contrast)
- Superadmin dashboard includes a theme editing page for live updates to site appearance
- Mobile-first, responsive design for all user-facing and admin pages
- UI/UX informed by best practices and world-class design standards

## Out of Scope (for MVP)
- Exporting player lists (to be evaluated)
- Advanced graphical court layouts (initially table-based)
- Deep stats/rankings (basic participation tracking only)
- Apple social login (for now)
- User journey maps and wireframes (to be developed in future design phase)

## Open Questions / To Be Determined
- Finalize feature set for free vs. premium tiers
- Export functionality for player lists
- Depth of DUPR/regional integration
- Club/organization onboarding and management flows
- Transition from Google AdSense to pickleball-centric ad system

## Success Criteria
- Users can sign up, create/manage events, and generate round robin schedules for singles/doubles
- Schedules minimize repeat matchups for supported group sizes
- Users can print or download schedules (with QR code)
- Notifications and group chat work as expected
- Clubs can manage members and events, with branding and directory
- PWA is usable on mobile devices and supports offline access
- RSVP, photo sharing, and privacy/safety features are available
- Admin tools support advanced club/org management
- Group home/landing page displays group info, photos, and conversations
- Testing is integrated and covers core features
- Superadmin dashboard includes theme editor and revenue analytics
- UI/UX is modern, accessible, and themeable with light/dark mode

---

*This PRD will be used to generate a detailed task list and guide the development of RoundRobinPro using the ai-dev-tasks workflow.* 