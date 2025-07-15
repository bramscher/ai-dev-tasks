# Product Requirements Document (PRD): Onboarding & Personalization

## 1. Product Vision & Goals

Build a profile-driven, personalized health platform that maximizes user engagement, retention, and monetization by leveraging deep onboarding, tailored recommendations, and expert-driven content.

## 2. Key Features & Requirements

### A. Profile as Gateway
- Users must complete a profile before accessing the main feed.
- Profile includes: health goals, supplement history, preferred learning style (video, article, podcast), and can be updated from the dashboard.

### B. Personalized Recommendations
- Use profile data to drive recommendations for content, apps, and experts.
- Map interests to app recommendations (e.g., sleep → Whattsupp + Remy).

### C. Custom Expert Email Feeds
- Weekly digests and real-time notifications for followed experts.
- Premium features tied to expert following.

### D. Engagement & Gamification
- Badges/progress bars for profile completion, following experts, trying features.
- Streaks for daily logins or supplement tracking.

### E. Social Proof
- Show stats like "X users with similar interests follow Dr. Huberman."
- Highlight popular stacks and trending content.

### F. Data Privacy & Controls
- Transparent data usage policies.
- Granular controls for email preferences and data sharing.

### G. Onboarding UX
- Wizard-style onboarding with progress indicators.
- Preview of personalized feed as users select interests/experts.

### H. Analytics
- Track which profile fields/features drive engagement and conversions.
- Use analytics to iterate on onboarding and recommendations.

### I. Experts Video Cross-Referencing ✅ **IMPLEMENTED**
- **Video-Expert Discovery Engine**: ✅ **COMPLETED** - Users can discover experts through video content browsing, with accurate video counts displayed for each expert on expert cards
- **Expert Video Filtering**: ✅ **COMPLETED** - Implemented dropdown filtering on video summaries page that shows only experts with available video content and proper video counts
- **Expert Video Feeds**: ✅ **COMPLETED** - Users can filter video summaries by specific experts to view dedicated expert content feeds
- **Video-Based Expert Discovery**: ✅ **COMPLETED** - Expert cards now display video summary counts alongside recommendation counts for better expert evaluation
- **Smart Video Categorization**: ✅ **COMPLETED** - Video summaries are categorized and can be filtered by category, search terms, and expert selection
- **Video Content Summarization**: ✅ **COMPLETED** - AI-generated summaries are available for expert videos with proper metadata and searchability
- **Expert Video Analytics**: 🔄 **IN PROGRESS** - Basic video count tracking implemented, engagement metrics tracking to be enhanced
- **Cross-Platform Video Integration**: 🔄 **PLANNED** - Connect video content to supplement/nootropic/peptide recommendations mentioned by experts
- **Video-Based Expert Recommendations**: 🔄 **PLANNED** - Use video viewing history to suggest relevant experts using collaborative filtering

## 3. User Stories & Acceptance Criteria

### Core Functionality
- **As a new user**, I must complete my profile before accessing the feed, so that my experience is personalized.
- **As a user**, I want to update my profile from the dashboard, so my recommendations stay relevant.
- **As a user**, I want to see badges and progress bars, so I feel motivated to complete my profile and try features.
- **As a user**, I want to follow experts and receive custom email digests, so I stay engaged with relevant content.
- **As a user**, I want to control my data and email preferences, so I feel safe and respected.
- **As a user**, I want to see what's popular among similar users, so I can discover new content and features.

### Experts Video Cross-Referencing
- **As a user**, I want to discover experts through video content, so I can find relevant health professionals based on topics I'm interested in. ✅ **COMPLETED**
- **As a user**, I want to see how many videos an expert has published, so I can gauge their content volume and expertise. ✅ **COMPLETED**
- **As a user**, I want to access dedicated video feeds for experts I follow, so I can easily find their latest content. ✅ **COMPLETED**
- **As a user**, I want to search for videos by expert specialty, so I can find content relevant to my health goals. ✅ **COMPLETED**
- **As a user**, I want to receive video summaries, so I can quickly understand the key points without watching full videos. ✅ **COMPLETED**
- **As a user**, I want to receive video recommendations based on experts I follow, so I can discover related content. 🔄 **PLANNED**
- **As a user**, I want to see which supplements/nootropics/peptides are mentioned in expert videos, so I can make informed decisions. 🔄 **PLANNED**
- **As a user**, I want to see expert authority metrics (views, engagement), so I can trust the credibility of their content. 🔄 **PLANNED**

## 4. Technical Requirements

### Core Platform
- Profile schema: health goals, supplement history, learning style, editable from dashboard.
- Recommendation engine MVP: rule-based mapping of profile to content/apps/experts.
- Email infrastructure: transactional and digest emails, real-time notifications.
- Gamification: badges, progress bars, streak tracking.
- Analytics: event tracking for onboarding, profile updates, feature usage.
- Privacy: user controls for data and email preferences.
- Onboarding UI: wizard flow, progress indicators, preview feed.

### Experts Video Cross-Referencing System ✅ **PARTIALLY IMPLEMENTED**
- **Database Schema**: ✅ **COMPLETED**
  - Enhanced experts table with video_count, engagement_metrics, specialties
  - Video-expert mapping through channel_id relationships
  - Video metadata including categories, AI-generated summaries, and content matching
  - Video viewing history tracking for personalization 🔄 **PLANNED**
- **Video Discovery Service**: ✅ **COMPLETED**
  - `getExpertsWithVideoSummaries()` function for retrieving experts with video counts
  - `getExpertVideosCounts()` function for accurate video count filtering
  - Video filtering by expert name with exact matching
  - Video search functionality with expert and content matching
  - Category-based video filtering and sorting options
- **Content Processing**: ✅ **COMPLETED**
  - Video transcription and summarization pipeline
  - Automatic categorization and tagging of video content
  - Expert-video association through channel_id mapping
  - Product mention extraction from video content 🔄 **PLANNED**
- **UI/UX Implementation**: ✅ **COMPLETED**
  - Expert dropdown filtering with dynamic video counts
  - Video summaries page with proper expert filtering
  - Expert cards displaying video summary counts
  - Responsive design with improved dropdown sizing
  - Search and filter functionality with debounced input
- **Recommendation Engine**: 🔄 **PLANNED**
  - Video-based expert recommendations using collaborative filtering
  - Expert-based video recommendations using user preferences
  - Cross-platform content recommendations (videos → supplements/nootropics/peptides)
- **Analytics & Metrics**: 🔄 **PLANNED**
  - Video engagement tracking (views, time watched, saves, shares)
  - Expert authority scoring based on video performance
  - User behavior analysis for recommendation improvements
- **API Endpoints**: 🔄 **PARTIALLY IMPLEMENTED**
  - Video summaries API with expert filtering ✅ **COMPLETED**
  - Expert video counts API ✅ **COMPLETED**
  - `/api/recommendations/videos` - Get personalized video recommendations 🔄 **PLANNED**
  - `/api/recommendations/experts` - Get expert recommendations based on video history 🔄 **PLANNED**

## 5. Next Steps

1. Design onboarding UI/UX (wireframes, Figma, etc.)
2. Define and implement profile schema (fields, types, validation)
3. Set up email infrastructure (transactional + digest)
4. Build recommendation engine MVP
5. **Implement experts video cross-referencing system**: ✅ **PHASE 1 COMPLETED**
   - ✅ Enhanced database schema for video-expert relationships
   - ✅ Built video discovery and filtering APIs
   - ✅ Created expert video feeds with proper filtering
   - ✅ Implemented video content processing pipeline
   - ✅ Built responsive UI with expert dropdown filtering
   - ✅ Integrated video counts into expert cards
6. **Phase 2 - Advanced Video Features**: 🔄 **NEXT PRIORITY**
   - Implement video-based expert recommendations using collaborative filtering
   - Add video engagement tracking and analytics dashboard
   - Create cross-platform recommendations (videos → supplements/nootropics/peptides)
   - Add video viewing history tracking for personalization
   - Implement expert authority scoring based on video performance
7. Implement gamification and social proof features
8. Add analytics tracking
9. Test with a small user group and iterate

## 6. Open Questions & Risks

- What profile fields drive the most engagement? (To be validated via analytics)
- How to balance onboarding depth with user drop-off risk?
- What privacy controls are most important to users?
- What are the technical constraints for real-time recommendations and notifications?
- **How to handle video content processing at scale?** (Transcription, summarization, categorization)
- **What metrics best indicate expert authority and content quality?**
- **How to prevent expert gaming of the video recommendation system?**
- **What's the optimal balance between expert video content and other content types?**

## 7. Success Metrics

### Core Platform
- Profile completion rate > 80%
- User retention (Day 7) > 40%
- Expert following rate > 60%
- Email open rate > 25%

### Experts Video Cross-Referencing ✅ **MEASURABLE WITH CURRENT IMPLEMENTATION**
- Video discovery rate: % of users who discover experts through video content ✅ **CAN MEASURE**
- Expert video filtering usage: % of users who use expert dropdown filtering ✅ **CAN MEASURE**
- Video search engagement: % of users who search for specific video content ✅ **CAN MEASURE**
- Expert card video count influence: Impact of video counts on expert profile clicks ✅ **CAN MEASURE**
- Expert video engagement: Average time spent watching expert videos 🔄 **REQUIRES ADDITIONAL TRACKING**
- Video-to-expert conversion: % of video viewers who follow the expert 🔄 **REQUIRES ADDITIONAL TRACKING**
- Cross-platform conversion: % of video viewers who try recommended products 🔄 **REQUIRES ADDITIONAL TRACKING**
- Expert authority accuracy: User satisfaction with expert recommendations 🔄 **REQUIRES ADDITIONAL TRACKING**

---

## 8. Recent Implementation Summary (Latest Update)

### ✅ **COMPLETED - Experts Video Cross-Referencing Phase 1**

**Key Features Implemented:**
- **Expert Video Discovery**: Users can now discover experts through video content with accurate video counts displayed on expert cards
- **Smart Video Filtering**: Advanced dropdown filtering on video summaries page that shows only experts with available content and displays real-time filtered counts
- **Expert Video Feeds**: Users can filter video summaries by specific experts to view dedicated expert content streams
- **Enhanced Expert Cards**: Expert profile cards now show video summary counts alongside recommendation counts for better expert evaluation
- **Responsive Design**: Improved UI with larger expert dropdown (280px width) and optimized search input layout
- **Exact Expert Matching**: Fixed expert filtering to use exact name matching for accurate video retrieval

**Technical Achievements:**
- Enhanced `getExpertVideosCounts()` function with proper filtering support
- Implemented exact expert lookup using channel_id relationships
- Built responsive video summaries page with multi-filter capabilities
- Integrated video counts into expert discovery flow
- Added comprehensive logging and debugging for video-expert relationships

**User Experience Improvements:**
- Cleaner expert cards that only show recommendation counts when > 0
- Better video discovery through expert-based filtering
- Improved search and filtering performance with debounced inputs
- Enhanced dropdown usability with increased height limits

**Next Phase Priorities:**
- Video-based expert recommendations using collaborative filtering
- Advanced video engagement tracking and analytics
- Cross-platform recommendations (videos → supplements/nootropics/peptides)
- Video viewing history tracking for personalization

---

*This PRD is based on the Feature Product Brief and is intended as a living document to guide onboarding and personalization feature development.* 