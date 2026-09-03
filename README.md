# DCISM_Unified

Problem Statement:
During enrollment, students may experience long and uncertain waiting times when seeking assistance for concerns such as unavailable subjects, section conflicts, lack of slots, and petitioned courses. Although queueing systems help organize students, they may still be left without a clear idea of when they will actually be accommodated. This can result in students waiting for long periods, repeatedly checking for updates, or missing the proper time to address their enrollment concerns.

Students may also need to frequently monitor ISMIS or separate announcements to know whether additional slots or petitioned courses have become available. The absence of a centralized and timely notification system makes the enrollment process less convenient and can cause delays in completing enrollment requirements.

To address these issues, DCISM_Unified aims to provide students with estimated accommodation time slots for enrollment concerns and send notifications regarding important enrollment updates, such as available course slots and petitioned courses, while coordinating with the existing Hermes Queueing System.


Proposed solution:
# DCISM_Unified: A Centralized Notification System that Fetches from the School’s ISMIS, Hermes, and Professor’s Updates on Enrollment Statuses

Students can receive alerts when:
     - Their estimated enrollment assistance time is approaching
     - Their queue number is about to be called through integration with the Hermes Queueing System
     - A slot becomes available in a requested course 
     - A petitioned Course is approved or opened
     - An enrollment concern changes status
     - A simultaneous, course equivalency, override request changes status 
     - An important enrollment deadline is approaching 
     - Student leaders or representatives can post and notify enrollment updates.

By:
Bacolod, Zach Michael - BSIT 3
Jankovic, Mirko - BSIT 3
Medina, Karl Emmanuel - BSIT 3
Nuñeza, Oieu Zhydd - BSIT 
Segundino, Allyn James - BSIT 3


1. The Problem

     During enrollment, DCISM students often experience long waiting times and uncertainty when dealing with enrollment concerns such as unavailable subject slots, petitioned courses, and other registration issues. Students may need to repeatedly check ISMIS, contact the department, or wait in long queues without knowing when their concern will be addressed.

     This creates unnecessary delays, confusion, and inconvenience for both students and department staff. DCISM_Unified aims to solve this problem by improving how enrollment concerns and updates are communicated and managed, making the process more organized, efficient, and convenient for students.

2. Target Users

     The primary target users of DCISM_Unified are students under the Department of Computer, Information Sciences and Mathematics (DCISM) who experience enrollment-related concerns. These include students who need to request additional course slots, follow up on petitioned subjects, resolve enrollment issues, or wait for assistance from the department.

     The application is especially useful for students who currently have to repeatedly check ISMIS, contact department personnel, or wait in long queues without knowing when their concern will be accommodated. Through DCISM_Unified, students can receive notifications about available slots, updates on petitioned courses, and an estimated time when their enrollment concern can be handled.
Secondary users include DCISM faculty and administrative staff, who can use the system to organize student concerns, provide updates, and manage the enrollment queue more efficiently.

3. Existing Solutions

	a. ISMIS - 
		ISMIS serves as the university’s primary student information and enrollment platform. Students use it to access official enrollment information, view subjects and schedules, and perform enrollment-related transactions.
 		Although ISMIS contains important information, students may still need to repeatedly open the platform to determine whether a course slot has become available or whether enrollment information has changed. It primarily serves as a system for managing official student records and 				transactions rather than as a personalized notification system for every enrollment concern.


	b. Hermes Queueing System -
		The Hermes Queueing System helps organize students seeking assistance from university personnel. It provides a structured queue and prevents students from forming an unorganized physical line during enrollment.
		However, queue organization does not completely remove uncertainty. Students may still be unsure how long they must wait, when they should return, or whether the processing of earlier concerns will delay their turn. Hermes also focuses mainly on queue management and does not necessarily 		cover course-slot availability, petitioned courses, override requests, course equivalency, simultaneous enrollment requests, or enrollment deadlines.


	c. College of Computer Studies queuing and electronic bulletin system

	Outside of the institution's already implemented and relating systems, there is also an existing platform made available by the College of Computer Studies of Central Philippine University (CPU), Iloilo City, intended to aid 	the enrolment processes of students as well as provide a proper queuing system to systematically improve the situation.

	Their system includes important modules that the DCISM Department currently needs, such as an electronic bulletin where announcements regarding concerns and enrollment updates within the department are posted.

	This is relevant to our proposed system as it serves as a perfect guide and blueprint of what the department desperately needs in order to fix the current issues faced especially in the enrollment period.

	Reference: https://repository.cpu.edu.ph/handle/20.500.12852/2257

4. What Makes Your App Different?

	DCISM_Unified is different because it combines enrollment-related updates from multiple sources into one student-centered notification platform. Instead of replacing ISMIS, Hermes, or existing communication channels, it works as a connecting layer between them.

	Furthermore, it is distinct from the systems aforementioned as it is built to solve one particular narrow problem, i.e., helping students track and get notified about ongoing enrollment concern updates such as newly opened course schedules, recently available courses from petitions, petitioned courses' statuses, queuing notifier, and many more, which the systems lack.

5.  Feasibility Check 
	Budget — Feasible at ₱0–low cost. Core stack (Firebase/Supabase for backend + auth, free tiers) covers notifications, database, and hosting for a student-scale user base. Main cost risk is if USC requires official ISMIS/Hermes API access or a dedicated server — likely absorbed by the university if this becomes a sanctioned integration, not an out-of-pocket group expense.

	Time — Tight but doable for a semester-long project. Riskiest part isn't the app itself, it's getting real coordination/data access from ISMIS and the Hermes Queueing system — that dependency could stall development if USC IT doesn't grant access early. Recommend building against mocked/sample data first, then integrating live data once access is confirmed.

	Skills — Well within the group's current stack: React Native/Expo for the mobile app, Firebase or Supabase for real-time notifications and auth, MySQL if a relational schema is needed for slot/queue data.

	Technology — The main technical risk is integration, not the app UI.
		1. Official integration — USC/ISMIS or Hermes exposes an API/webhook you can subscribe to for real-time slot and petition status, but depends entirely on 		   institutional approval.
		2. Workaround (scraping/polling) — periodically checking ISMIS for changes, doable without official access, but fragile (breaks if ISMIS changes its 			   layout).

