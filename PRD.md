# Illumine Classroom

**Product note and experiment log**

[Open the mobile prototype](index.html). Use the prefilled credentials to sign in as Emma Wilson. Chandler Reed has the richest sample record and is the best starting point.

## Problem and scope

Teachers need to record naps, share group moments, and capture meal intake while supervising a room. The goal is to reduce **active phone time per completed classroom task** while preserving who recorded what, when it happened, and which families received it.

We started with four classrooms of ten students and considered teacher coverage. The current prototype follows **one teacher and ten assigned students in Willow Room**. Quick actions handle the room. Student profiles handle one child’s care information, records, and updates.

## What the research established

| Product | Published workflow | What informed this prototype |
| --- | --- | --- |
| **Illumine** | Mobile teachers can select children to start and end naps. Daily reports can include nap details. | Reuse the room roster, familiar nap actions, and existing family update patterns. [Teacher guide](https://help.illumine.app/en/articles/14003306-illumine-app-teacher-user-guide) · [Daily reports](https://help.illumine.app/en/articles/13764166-daily-reports) |
| **Brightwheel** | Staff log sleep observations against an active nap. Web entry supports several students, with records by room or child. | Capture structured observations and preserve an attributable record. [Sleep-check guide](https://help.mybrightwheel.com/en/articles/5520776-log-student-sleep-checks) |
| **Procare** | Nap reminders can repeat. The activity dashboard shows who is sleeping and when naps began. | Make room state and due times visible at a glance. [Nap activities](https://www.procaresupport.com/procare-online/docs/nap-activities) · [Activity dashboard](https://www.procaresupport.com/procare-online/docs/viewing-the-activity-dashboard) |
| **Famly and Storypark** | Famly supports room-based checks and documents a sleep report. Storypark keeps sleep checks staff-visible and shares sleep start and end with families. | Give staff detailed records and families information suited to their view. [Famly sleep and reporting](https://help.famly.co/en/articles/4912350-recording-when-children-sleep) · [Storypark routines](https://help.storypark.com/en/articles/4580658-educators-routines) |
| **NestliCare** | Its care board highlights due checks, supports a whole-room shortcut, and reports gaps. | A queue alone is established. Test whether shorter entry and clearer handoffs reduce actual classroom work. [Sleep-check workflow](https://help.nestlicare.com/owners/faq/where-are-infant-sleep-checks) |

**U.S. timing context.** States and territories set licensing requirements. The applicable rule depends on age, jurisdiction, and care setting. Washington specifies visible checks every 15 minutes for infants alongside active supervision. North Dakota’s licensing manual specifies visual checks every 10–15 minutes for sleeping infants. The prototype models a 15-minute policy: first check from actual sleep onset, subsequent checks from the last actual observation. Noon to 1 PM is a display window. A child still asleep after 1 PM remains in the queue. The teacher performs the physical observation and records it. A real pilot requires a verified room policy and required observation fields. [Federal licensing overview](https://www.childcare.gov/consumer-education/regulated-child-care) · [Washington rule](https://apps.leg.wa.gov/wac/default.aspx?cite=110-300-0291) · [North Dakota licensing manual](https://www.hhs.nd.gov/cfs/early-childhood-services/licensing-policy-manual) · [California safe-sleep guidance](https://cchp.ucsf.edu/resources/forms-policies-and-checklists/safe-sleep-policy-infants-child-care)

## Walk through the current prototype

### 1. Classroom and student profile

**Sign in → Classroom.** Emma’s name leads the header, with **10 assigned students · Willow Room** beneath it and the official Illumine wordmark opposite. **Nap rounds** and **Group update** sit side by side. **Meal status** is the same size on the second row. The two-column student grid scrolls independently. Chandler has a fictional portrait. Other tiles use initials.

**Chandler Reed → Student profile.** The portrait, name, classroom, and teacher come first. The **Care information** card shows a sample peanut allergy, emergency contact, age, and B positive blood group. Unknown data is marked as such. The main cards open **Nap record**, **Kid Activity**, and **Meal status**. **Attendance** and **Fee structure** open dismissible coming-soon messages.

### 2. Nap rounds and nap record

**Quick actions → Nap rounds.** The compact list shows the current demo time and sorts sleeping children by their next check. Overdue, due, and sleep states use text. **Mark asleep** starts a child’s clock. **Mark awake** ends future checks and retains the history.

**Log check** opens one child’s form. The noon-to-1 timeline shows sleep onset and green ticks at recorded check times. The teacher records sleep position, breathing, signs of distress, and optional notes. **Observed at** defaults to the current demo time. **Change** opens a one-minute scroll wheel, also used by the sleep and wake sheets. Closing a sheet discards unsaved changes. A check stores its deadline, observation time, entry time, teacher, and findings. Concerns surface the center’s response prompt.

**Student profile → Nap record** shows seven days. Today’s active nap has its own **In progress** card with **Log sleep check**, **Mark awake**, and an expandable check log. Prior days expand to show start and wake times and each check’s timing, observations, and author. Missing entries remain visible. Try Chandler’s overdue check: he fell asleep at 12:02, was due at 12:17, and recording at 12:18 sets the next check for 12:33.

### 3. Group updates and Kid Activity

**Quick actions → Group update → Use sample photo → Choose students.** A teacher can also capture or choose a photo or video, add a caption, select the students, and confirm sharing. **Sent group updates** below the composer shows the media, caption, teacher, timestamp, and original recipient list.

**Student profile → Kid Activity** shows sent activities newest first and offers **Create update** for that child’s family. Chandler has sample block play, rhymes, and story-time posts. **Remove** in a child’s feed affects only that child. **Delete** in the group log confirms removal for every recipient. Back from the child’s feed goes through the profile to the classroom, skipping the send receipt.

### 4. Meals

**Quick actions → Meal status → Today’s lunch.** **Share menu** offers **Take photo**, **Choose photo**, and **Use sample photo**. Select menu items such as salad, beans, vegetables, or bread, add an optional note, then review and share with all ten families. The menu is displayed in each child’s **Meal status → Today**.

**Record intake** is a separate tab. Tap **Didn’t eat**, **Partially ate**, or **Fully ate** per student. The same staff record is editable from the child’s **Meal status**, where each of the last seven days expands to show its menu and any available photo. Chandler has two sample menus, one with the lunch illustration. Missing records show **Not recorded**. Shared menus exclude individual intake and appear only under Meal status.

## Iteration log and open questions

| We tried or considered | Decision |
| --- | --- |
| Fixed classroom checkpoints, a round sheet, and a guided round | Use child-specific deadlines and direct row actions. Keep the due-sorted room list compact. |
| A timeline on every row and a demo-clock control | Put the timeline inside **Log check**, retain a read-only current time on the roster, and use a scroll wheel for time edits. |
| Several home layouts and alert treatments | Match quick-action cards, keep identity compact, and put a restrained allergy label in care information below the child’s identity. |
| Voice entry, crib-order grouping, and cross-teacher handoff | Keep as experiments. Compare voice with taps for exception notes. Test room-order grouping and handoff against a due-sorted roster before adding them. |
| Parent nap summaries and principal sleep reports | Considered separate audience views. The current prototype demonstrates recipient histories and teacher-facing records. |

**Validation.** Compare active phone seconds per round, repeat trips, on-time observations, and correct attribution. For sharing, test recipient selection, single-child removal, and group-wide deletion. For meals, verify that sharing leaves intake unchanged. Open production questions include offline save and retry, duplicate or concurrent edits, audited corrections, and role-based access.

**Demo boundary.** Fictional data, sample credentials, simulated family delivery, and state that resets on reload. No backend or live family accounts are connected. The design takes brand cues from [Illumine](https://illumine.app/) and keeps the same mobile spacing, touch targets, and controls across the flows.
