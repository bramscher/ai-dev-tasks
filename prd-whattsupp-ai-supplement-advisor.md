# Product Requirements Document: WhattsSupp AI Supplement Advisor

## 1. Introduction/Overview

WhattsSupp is an AI-powered supplement advisor that provides personalized supplement recommendations based on comprehensive user health profiles and ongoing conversations. The system maintains persistent memory across sessions to build increasingly accurate and personalized recommendations over time.

**Problem Statement:** Users struggle to navigate the complex world of supplements due to information overload from podcasts, conflicting expert opinions, and lack of personalized guidance. Most people spend hours researching supplements without finding clear, evidence-based recommendations tailored to their specific needs.

**Solution:** An AI assistant that analyzes expert podcast summaries and research to provide personalized, evidence-based supplement recommendations in minutes instead of hours, with continuous learning from user interactions and supplement journeys.

## 2. Goals

### Primary Goals
1. **Reduce Research Time**: Cut supplement research time from hours to minutes through AI-powered expert analysis
2. **Increase Recommendation Accuracy**: Achieve 85%+ user satisfaction with AI recommendations through personalized profiling
3. **Build User Engagement**: Maintain 70%+ monthly active user rate through conversational interface and progress tracking
4. **Drive Conversions**: Achieve 15%+ conversion rate from recommendations to purchases through integrated shopping features

### Secondary Goals
1. **Expert Content Utilization**: Leverage 50+ health expert podcast summaries for evidence-based recommendations
2. **Cross-Product Integration**: Integrate with other Wellifi apps (Remy, AIWorx) for holistic health recommendations
3. **Data Quality**: Build comprehensive user profiles with 90%+ completion rates
4. **Safety Compliance**: Maintain zero medication interaction warnings through robust safety checks

## 3. User Stories

### Core User Journey
- **As a new user**, I want to complete a comprehensive health profile so that I can receive personalized supplement recommendations tailored to my specific needs
- **As a returning user**, I want the AI to remember our previous conversations so that I don't have to repeat my health information
- **As a user seeking recommendations**, I want to have a natural conversation about my health goals so that I feel understood rather than interrogated by forms
- **As a supplement beginner**, I want evidence-based explanations for each recommendation so that I can make informed decisions about my health

### Advanced Features
- **As a user tracking supplements**, I want to log my supplement effectiveness over time so that the AI can refine future recommendations
- **As a cost-conscious user**, I want to see price comparisons and budget-friendly alternatives so that I can make financially responsible choices
- **As a safety-conscious user**, I want automatic medication interaction checking so that I can avoid potentially dangerous combinations
- **As a progress-oriented user**, I want regular check-ins and progress reports so that I can track my supplement journey

### Shopping & Management
- **As a user ready to purchase**, I want streamlined shopping with pre-filled carts so that I can easily buy recommended supplements
- **As a busy user**, I want subscription management for regular supplements so that I never run out of my essential supplements
- **As an organized user**, I want to categorize supplements across multiple lists so that I can manage current, future, and past supplements effectively

## 4. Functional Requirements

### 4.1 Enhanced User Profile System ⚡ **PARTIALLY IMPLEMENTED**
**Status**: Basic profile exists, needs enhancement

1. **Extended Health Data Collection**
   - Current: age, gender, medications, allergies, notes, activity level, height, weight, weight loss goal ✅
   - **NEW**: Multiple health concerns/goals (unlimited), chronic conditions, family health history
   - **NEW**: Diet type (vegetarian, keto, etc.), exercise frequency, sleep patterns, stress levels
   - **NEW**: Substance use tracking (alcohol, smoking), compliance history

2. **Supplement History Tracking**
   - **NEW**: Currently taking supplements with dosage, timing, duration
   - **NEW**: Previously tried supplements with effectiveness ratings (1-5 scale)
   - **NEW**: Side effects experienced, brand preferences
   - **NEW**: Compliance tracking and adherence patterns

3. **Goals & Preferences Management**
   - **NEW**: Health improvement goals with specific timelines
   - **NEW**: Budget constraints and price sensitivity
   - **NEW**: Preferred supplement forms (capsules, powder, liquid)
   - **NEW**: Shopping preferences and subscription willingness

### 4.2 Conversation Memory System ⚡ **NEEDS ENHANCEMENT**
**Status**: Basic chat history exists, needs persistent cross-session memory

4. **Session Management**
   - **ENHANCE**: Store conversation history in database with user associations
   - **NEW**: Unique conversation IDs with topic categorization
   - **NEW**: Progress markers and follow-up scheduling

5. **Context Retention**
   - **ENHANCE**: Remember previous recommendations and user responses (accepted/rejected/questioned)
   - **NEW**: Track recommendation patterns and user preferences over time
   - **NEW**: Maintain unresolved questions and follow-up items

6. **Learning Accumulation**
   - **NEW**: Identify patterns in user preferences and effectiveness trends
   - **NEW**: Track sensitivity discoveries and optimal timing/dosage findings
   - **NEW**: Build complexity progression (basic → advanced recommendations)

### 4.3 Enhanced Recommendation Engine ⚡ **PARTIALLY IMPLEMENTED**
**Status**: Basic AI recommendations exist, needs sophisticated enhancement

7. **Advanced Input Processing**
   - Current: User profile, health categories, conversation context ✅
   - **ENHANCE**: Expert podcast summaries database integration
   - **NEW**: Clinical research database integration
   - **NEW**: Drug-supplement interaction database checking

8. **Sophisticated Recommendation Logic**
   - **ENHANCE**: Primary issue matching with weighted evidence scoring
   - **NEW**: Personalization filters (allergens, interactions, budget, past effectiveness)
   - **NEW**: Synergy optimization for complementary supplements
   - **NEW**: Timing optimization recommendations

9. **Comprehensive Output Structure**
   - Current: Basic supplement name, description, type ✅
   - **ENHANCE**: Recommended dosage ranges and optimal timing
   - **NEW**: Expected benefits and evidence levels (High/Medium/Low)
   - **NEW**: Expert sources with citations and potential side effects
   - **NEW**: Price ranges and confidence scores

### 4.4 Enhanced Supplement List Management ⚡ **PARTIALLY IMPLEMENTED**
**Status**: Basic save/remove functionality exists, needs full list management

10. **Currently Taking List**
    - Current: Basic save to user_products table ✅
    - **ENHANCE**: Active supplements with dosage and schedule tracking
    - **NEW**: Effectiveness tracking with 1-5 scale ratings
    - **NEW**: Compliance monitoring and refill reminders
    - **NEW**: Quick reorder functionality

11. **Suggested List Management**
    - Current: AI recommendations display ✅
    - **ENHANCE**: Persistent suggested list with priority ranking
    - **NEW**: Research links and expert source citations
    - **NEW**: "Why recommended" explanations for each item

12. **Shopping Cart Integration**
    - **NEW**: Items ready for purchase with quantity selection
    - **NEW**: Price comparisons across vendors
    - **NEW**: Subscription frequency options
    - **NEW**: Bundle suggestions for cost savings

13. **History Tracking**
    - **NEW**: Previously used supplements with duration and effectiveness
    - **NEW**: Discontinuation reasons and "would retry" flags
    - **NEW**: Export functionality for healthcare providers

### 4.5 Shopping Cart & Purchase Integration 🆕 **NEW FEATURE**

14. **Cart Functionality**
    - Add items from suggested list or search
    - Quantity and size selection with subscription options
    - Real-time price comparison across vendors
    - Shipping cost calculation and coupon application

15. **Vendor Integration**
    - Multiple vendor pricing APIs
    - Direct checkout links with affiliate tracking
    - Inventory status and shipping estimates
    - Purchase history and spending analytics

16. **Subscription Management**
    - Auto-reorder scheduling for regular supplements
    - One-click reorder for frequently used items
    - Bundle creation for cost optimization
    - Subscription modification and cancellation

### 4.6 Progress Tracking System 🆕 **NEW FEATURE**

17. **Effectiveness Tracking**
    - Subjective effectiveness ratings (1-5 scale)
    - Symptom improvement tracking over time
    - Side effect logging and compliance percentage
    - Cost per month analysis

18. **Check-in System**
    - Automated reminders at optimal intervals (1 week, 1 month, 3 months)
    - Quick rating interface with detailed feedback options
    - Photo progress tracking (optional)
    - Biomarker integration capability for future expansion

19. **Analytics Dashboard**
    - Effectiveness trends over time with visual charts
    - Cost-benefit analysis and ROI calculations
    - Compliance pattern analysis
    - Supplement correlation insights

20. **Reporting Features**
    - Monthly progress summaries via email
    - Healthcare provider reports (PDF export)
    - Goal achievement metrics and recommendations
    - Budget tracking with spending insights

### 4.7 Enhanced AI Conversation Interface ⚡ **PARTIALLY IMPLEMENTED**
**Status**: Basic conversation exists, needs memory and advanced features

21. **Advanced Conversation Capabilities**
    - Current: Natural language understanding and context-aware responses ✅
    - **ENHANCE**: Reference previous conversations naturally
    - **NEW**: Build on established preferences and track conversation goals
    - **NEW**: Adjust complexity to user knowledge level

22. **Memory Integration Features**
    - **NEW**: "Remember when we talked about..." references
    - **NEW**: Acknowledge user feedback from previous sessions
    - **NEW**: Avoid redundant recommendations automatically

23. **Enhanced Response Features**
    - Current: Basic product recommendations ✅
    - **ENHANCE**: Specific expert source citations
    - **NEW**: Research summary links and alternative options
    - **NEW**: Detailed reasoning explanations

## 5. Non-Goals (Out of Scope)

### Version 1.0 Exclusions
1. **Medical Diagnosis**: WhattsSupp will not diagnose medical conditions or replace medical advice
2. **Prescription Management**: No prescription medication recommendations or management
3. **Telehealth Integration**: No direct healthcare provider video calls or consultations
4. **Complex Biomarker Analysis**: Advanced lab result interpretation beyond basic tracking
5. **International Shipping**: Focus on US market only for initial launch

### Future Version Considerations
1. **Social Features**: Supplement sharing, user communities, or social recommendations
2. **Wearable Integration**: Direct integration with fitness trackers or health monitors
3. **Advanced AI Features**: Image recognition for supplement bottles or packaging
4. **Multi-language Support**: Non-English language interfaces

## 6. Design Considerations

### UI/UX Requirements [[memory:2330311]] [[memory:2330309]]
1. **Theme Consistency**: Follow Apple.com styled design with modern, pickleball-centric aesthetic
2. **Central Theme System**: All components reference centralized theme for consistent styling
3. **Responsive Design**: Mobile-first approach with adaptive layouts
4. **Accessibility**: WCAG 2.1 AA compliance for all interactive elements

### Current Layout Enhancement
1. **Three-Panel Interface** (Current ✅): Chat panel, profile panel, supplements panel
2. **Real-time Updates**: Seamless data synchronization across all panels
3. **Progressive Disclosure**: Advanced features revealed as users become more engaged
4. **Visual Hierarchy**: Clear separation between chat, recommendations, and management

### Component Integration
1. **Leverage Existing**: Build on current shadcn/ui components and Supabase integration
2. **Theme Integration**: Ensure all new components follow established design patterns
3. **Animation**: Subtle Framer Motion animations for enhanced user experience

## 7. Technical Considerations

### Current Architecture ✅ **IMPLEMENTED**
1. **Next.js 14**: App Router with server components
2. **Supabase**: Authentication, database, storage
3. **OpenAI Integration**: GPT-4 for conversations and recommendations
4. **Shadcn/UI**: Component library with consistent theming

### Database Enhancements Required
1. **New Tables Needed**:
   - `conversation_sessions` (session management)
   - `user_supplement_history` (tracking effectiveness)
   - `supplement_interactions` (safety database)
   - `user_preferences` (shopping, timing, budget)
   - `progress_tracking` (check-ins, effectiveness)

2. **Enhanced Existing Tables**:
   - Expand `profiles` table with additional health fields
   - Extend `user_products` with effectiveness tracking
   - Add conversation context to message history

### API Integrations
1. **Supplement Data**: iHerb, Vitacost, Amazon for pricing and availability
2. **Expert Content**: Existing podcast summary database
3. **Research Database**: PubMed, clinical trial databases
4. **Payment Processing**: Stripe for subscription management

### Performance Requirements
1. **Response Time**: Chat responses within 3 seconds
2. **Recommendation Generation**: Complete recommendations within 10 seconds
3. **Data Sync**: Real-time updates across all panels
4. **Scalability**: Support 10,000+ concurrent users

## 8. Success Metrics

### User Engagement
- **Daily Active Users**: Target 70% of monthly users
- **Session Duration**: Average 15+ minutes per session
- **Conversation Depth**: 10+ messages per conversation
- **Return Rate**: 60%+ users return within 7 days

### Health Outcomes
- **Recommendation Satisfaction**: 85%+ user approval ratings
- **Goal Achievement**: 70%+ users report progress toward health goals
- **Supplement Adherence**: 80%+ compliance with recommended regimens
- **Safety Incidents**: Zero reported medication interactions

### Business Metrics
- **Conversion Rate**: 15%+ from recommendation to purchase
- **Average Order Value**: $75+ per transaction
- **Customer Lifetime Value**: $300+ per user annually
- **Affiliate Revenue**: $50+ per active user per year

### Technical Metrics
- **System Availability**: 99.9% uptime
- **Response Time**: <3 seconds for chat responses
- **Data Accuracy**: <1% error rate in recommendations
- **User Satisfaction**: 4.5+ star rating in app stores

## 9. Open Questions

### Technical Implementation
1. How will we handle complex drug-supplement interactions beyond basic database lookups?
2. What level of medical review is required for AI-generated recommendations?
3. How do we balance personalization with privacy concerns for health data?

### Business Model
1. What percentage of revenue should come from affiliate commissions vs. subscriptions?
2. How do we structure premium features to maximize user value and business revenue?
3. What partnerships with supplement brands or healthcare providers should we prioritize?

### User Experience
1. How do we onboard users who are completely new to supplements without overwhelming them?
2. What's the optimal frequency for progress check-ins to maintain engagement without being annoying?
3. How do we handle users who want to deviate from AI recommendations based on their own research?

### Regulatory and Safety
1. What disclaimers and safety warnings are required for AI-generated health recommendations?
2. How do we ensure compliance with FDA regulations regarding supplement recommendations?
3. What data retention and privacy policies are needed for health information storage?

---

## Implementation Priority

### Phase 1 (Weeks 1-4): Foundation Enhancement
- **Enhanced user profile system** with additional health fields (diet, exercise, sleep)
- **Persistent conversation memory** - basic session storage and context retention
- **Improved recommendation engine** - better matching and basic evidence scoring
- **Enhanced supplement lists** - better organization of current/suggested/history

### Phase 2 (Weeks 5-8): Core Functionality 
- **Basic progress tracking** - effectiveness ratings and simple check-ins
- **Conversation memory enhancement** - cross-session context and preference learning
- **Simple shopping features** - basic cart and affiliate link integration
- **Medication interaction warnings** - basic safety database integration

### Phase 3 (Weeks 9-12): Advanced Features
- **Comprehensive progress tracking** - detailed analytics and reporting
- **Advanced AI personalization** - expert source citations and evidence levels
- **Enhanced shopping** - price comparisons and subscription management
- **Basic vendor integration** - 1-2 major supplement retailers

### Phase 4 (Weeks 13-16): Sophisticated Systems
- **Full vendor marketplace** - multiple retailer integrations and real-time pricing
- **Comprehensive analytics dashboard** - detailed insights and health outcome tracking
- **Advanced safety features** - clinical research database integration
- **Healthcare provider tools** - export functionality and professional reports

### Future Phases (Post-Launch):
- **Complex AI features** - biomarker integration, advanced interaction analysis
- **Enterprise features** - practitioner dashboards, bulk recommendations
- **Advanced integrations** - wearable devices, telehealth platforms
- **Social features** - community recommendations, expert Q&A 