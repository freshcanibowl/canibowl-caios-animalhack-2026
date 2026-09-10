# Public Architecture

## Overview

CaniBowl is an AI-driven pet health concept with science-based nutrition at its core. This AnimalHack submission demonstrates a public-safe architecture for connecting structured pet information, feeding observations, and AI-assisted guidance.

```text
Pet Parent
    │
    ▼
CaniBowl Pet Profile
    │
    ├── Pet identity & life stage
    ├── Weight / body-condition observations
    ├── Meal & feeding records
    └── Stool / health observations
    │
    ▼
Health & Nutrition Data Layer
    │
    ▼
AI Assistance Layer
    │
    ├── Profile interpretation
    ├── Nutrition-oriented guidance
    ├── Trend / observation summaries
    └── Safety guardrails
    │
    ▼
Pet Parent Dashboard / Report
    │
    ▼
Future: Nutritionist / Veterinary Review
```

## Public Demo Components

### 1. Pet Profile

The demo uses synthetic pet information such as species, age, weight, life stage, activity level, and known feeding considerations.

### 2. Health & Feeding Records

The data model is designed around observations that pet parents can record over time, including:

- meals and feeding patterns
- weight changes
- stool observations
- body-condition observations
- appetite and behaviour notes
- other non-diagnostic health observations

### 3. AI Assistance

The AI layer turns structured information into understandable observations and next-step guidance. The public demo focuses on demonstrating the workflow rather than exposing proprietary CAIOS implementation details.

### 4. Safety Layer

The system should distinguish between general nutrition guidance and veterinary diagnosis. Concerning symptoms or potentially urgent situations should be directed to a qualified veterinarian rather than presented as a diagnosis.

## Private / Public Boundary

```text
PRIVATE — Source of Truth
corwinlim/caios-2.0

        │
        │ reviewed whitelist export
        ▼

PUBLIC — AnimalHack Submission
freshcanibowl/canibowl-caios-animalhack-2026
```

The public repository is intentionally **not a mirror** of the private CAIOS repository. Proprietary source code, private infrastructure, credentials, internal documentation, and real customer/pet-owner data remain outside this repository.

## Future Architecture

The longer-term CaniBowl platform can evolve toward:

- personalised feeding plans
- longitudinal pet-health timelines
- AI-generated weekly and monthly summaries
- nutritionist workflows
- veterinary review and referral workflows
- computer-vision assisted body-condition observations
- wearable and activity data
- community and research feedback loops

These are roadmap concepts and should not be interpreted as features already validated or clinically deployed by this submission.
