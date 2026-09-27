# Data Model Specification

## Core Entities & Schema

### 1. Users
* `id` (UUID, PK)
* `email` (String, Unique)
* `password_hash` (String)
* `role` (Enum: `participant`, `judge`, `organizer`, `admin`)[cite: 10]

### 2. Events
* `id` (UUID, PK)
* `title` (String)
* `start_date` (Timestamp)
* `submission_deadline` (Timestamp)
* `tracks` (JSON / Relation)

### 3. Teams
* `id` (UUID, PK)
* `event_id` (UUID, FK)
* `name` (String)
* `invite_code` (String, Unique)[cite: 10]

### 4. Submissions
* `id` (UUID, PK)
* `team_id` (UUID, FK)
* `event_id` (UUID, FK)
* `title` (String)
* `description` (Text)
* `repo_url` (String)
* `status` (Enum: `draft`, `submitted`)[cite: 10]

## Import / Export Paths
* Database seeds can be automatically injected on startup via initialization scripts.
* Data export is supported via structured JSON/CSV dumps.
