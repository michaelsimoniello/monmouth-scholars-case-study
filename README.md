# Monmouth Scholars

[Monmouth Scholars](https://monmouthscholars.com/) is a local tutoring marketplace that connects families in Monmouth County, New Jersey with carefully matched peer tutors.

I co-founded and built the business around a simple idea: tutoring works better when the experience is designed for both sides of the marketplace. Parents need confidence, responsiveness, and a good match. Tutors need clarity, support, and a structure that helps them create great sessions.

This repository is a public product case study. The production codebase is private because it contains sensitive customer and tutor information, operational workflows, and private infrastructure. The material here is intentionally high-level and uses no real customer records or private credentials.

## At a glance

- Built and operated a tutoring marketplace serving **100+ families**
- Designed the parent journey from first inquiry through matching, scheduling, payment, and follow-up
- Designed the tutor journey, including vetting, onboarding, matching, scheduling, and ongoing coaching
- Created a continuous feedback loop by speaking with families after their first session and checking in regularly
- Used that feedback in weekly tutor conversations to improve the experience
- Built the product and operating infrastructure with **Next.js, Vercel, Supabase, Drizzle, Resend, CozyCal, and AI-assisted development with Codex**
- Continued iterating on the business through direct customer conversations rather than treating the initial launch as the finish line

## The problem

Traditional tutoring is often fragmented:

- Parents have to search through disconnected listings.
- Tutor quality and fit are difficult to evaluate from a profile alone.
- Scheduling and communication happen across multiple tools.
- Tutors may have strong subject knowledge but little support in creating a great student experience.
- The business learns too slowly if feedback is only collected when something goes wrong.

The product opportunity was not simply to create another directory. It was to make the entire interaction—from the first request to the first successful session—feel personal, organized, and trustworthy.

## Product hypothesis

A better tutoring service could be built by treating the parent and tutor experiences as one connected product.

If we:

1. Learn what the family actually needs,
2. Match them with a tutor who fits those needs,
3. Make scheduling and communication straightforward,
4. Check in after the first session,
5. Turn feedback into concrete coaching and service improvements,

then families should be more likely to continue, tutors should be better equipped to deliver strong sessions, and the marketplace should improve with every interaction.

## How the product works

### Parent experience

The parent flow was designed around reducing uncertainty:

1. A family submits a tutoring request or asks to work with a specific tutor.
2. Monmouth Scholars reviews the request and the student's needs.
3. We identify appropriate tutor options and confirm availability.
4. The parent and tutor are introduced and agree on a time.
5. The session is scheduled and payment is collected before the session.
6. After the first session, we contact the family to learn how it went and help them schedule the next session.

The key insight was that the first session is not the end of the funnel. It is the moment when the family decides whether the service is worth trusting again.

### Tutor experience

Tutors are not just supply in a marketplace. They are the people delivering the product.

The tutor experience included:

- Vetting and onboarding
- Matching students based on subject, level, personality, and availability
- Scheduling coordination
- Clear expectations around sessions
- Weekly conversations about what was working and what could improve
- Feedback from families translated into practical coaching

This created a reinforcing loop:

```
Family feedback
      ↓
Tutor coaching
      ↓
Better sessions
      ↓
Stronger family relationships and retention
      ↓
More useful feedback
```

## Customer discovery and feedback

The most valuable research method was direct contact with families.

I spoke with every family after their first session and checked in regularly afterward. Those conversations helped surface details that would have been easy to miss from a form or dashboard:

- Whether the tutor felt like the right personality fit
- Whether the student felt comfortable asking questions
- Whether the parent understood what happened during the session
- Whether scheduling was creating friction
- What would make the family want to continue

I brought those patterns into weekly tutor meetings. This made customer discovery operational rather than theoretical: feedback changed how tutors prepared, communicated, and taught.

## What I built

My role covered product, engineering, growth, and operations.

### Product and operations

- Defined the parent and tutor journeys
- Designed intake and matching flows
- Created the vetting and onboarding process
- Built the follow-up system after first sessions
- Developed the feedback loop between families and tutors
- Managed the operational details required to make a two-sided marketplace work

### Technical product

- Built and iterated on the public website
- Connected request forms to a database-backed workflow
- Added server-side data handling and notification flows
- Created foundations for tutor and administrator portals
- Added authentication and row-level security policies for protected workflows
- Kept secrets and sensitive operational data out of the client and public repository

### Growth and learning

- Tested messaging based on what families actually valued
- Used direct feedback to refine the service
- Focused on retention and relationship quality rather than optimizing only for first-session volume
- Treated every interaction as both a service moment and a product-learning opportunity

## Technical architecture

The production application is built with a modern, intentionally simple web stack:

- **Next.js / React** for the web application
- **Vercel** for hosting and deployment
- **Supabase Postgres** for application data
- **Drizzle ORM** for server-side database access
- **Supabase Auth** for tutor and administrator sign-in
- **Resend** for operational email notifications
- **CozyCal** and calendar workflows for scheduling coordination
- **Codex** and other AI coding tools to accelerate implementation, debugging, and iteration

At a high level:

```
Family or tutor request
          ↓
Next.js application
          ↓
Server-side request handling
          ↓
Supabase Postgres
          ↓
Operational notification
          ↓
Matching, scheduling, session, and follow-up
```

The application is designed so that a saved request is not lost just because a notification fails. That distinction matters in an operational product: data persistence and communication are separate responsibilities.

## Why the production repository is private

The production repository is not public because it contains or connects to information that should not be exposed, including:

- Customer and tutor data
- Private operational workflows
- Internal contact and scheduling information
- Database configuration and security policies
- Environment-specific infrastructure
- Secrets and service integrations

This case-study repository is the public layer: it explains the product, decisions, architecture, and learning without exposing private data.

## Results and lessons

The most important result was not a single feature launch. It was building a working feedback system around a real service.

The business grew to serve more than 100 families. More importantly, we learned that customer obsession is not just answering support messages. It means deliberately creating opportunities to hear from customers, recognizing patterns, and changing the product or service in response.

The biggest lessons were:

### 1. The service is the product

In a marketplace, the website is only one part of the experience. Matching, communication, scheduling, tutor preparation, and follow-up all shape whether the product works.

### 2. Both sides of the marketplace matter

Optimizing only for the parent can create a poor tutor experience. Optimizing only for tutor supply can create a poor family experience. The product has to make both sides successful.

### 3. Feedback is most valuable when it changes behavior

A customer interview is not useful just because it produces notes. It is useful when the insight changes a flow, a policy, a tutor's behavior, or the next product decision.

### 4. Small operational details compound

A follow-up call, a clearer intake question, a better tutor introduction, or a more reliable notification can materially change the experience when repeated across every family.

### 5. AI is an implementation multiplier, not a substitute for judgment

AI tools helped me move quickly through implementation and debugging. I still had to define the problem, evaluate tradeoffs, protect customer data, and decide whether the resulting product behavior was actually useful.

## What this repository intentionally does not include

This is not a copy of the production application. It does not include:

- Real customer or tutor records
- Private contact information
- Production credentials or environment variables
- Internal business operations
- Sensitive database contents
- An unreviewed export of the private source code

The goal is to make the product understandable without compromising the people who use it.

## Links

- **Live product:** [monmouthscholars.com](https://monmouthscholars.com/)
- **Founder:** [Michael Simoniello on LinkedIn](https://www.linkedin.com/in/michaelsimoniello/)
- **Related project:** [BeaconScanner](https://github.com/michaelsimoniello/beacon-scanner), a BLE-based workout equipment tracking prototype

## Why I built it

I wanted to understand what happens when a product is not just designed on paper but operated with real customers.

Monmouth Scholars taught me to:

- Start with the customer experience
- Make ambiguous problems concrete
- Build quickly enough to learn
- Care about both sides of a marketplace
- Use data without ignoring qualitative feedback
- Own the entire path from problem to solution

That is the product work I want to keep doing.
