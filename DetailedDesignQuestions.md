# Importand questions to ask for detailed design documentations:

There is no hard and fast rule on when a spec if appropriate.  It's a function of complexity, certainty, and risk.  This is a desciprtion of a proposed plan to solve a problem. This is a tool to ensure that the right work gets done. (Final design doc is about 3 paragraphs max - per feature/system/consideration)

A design docs main goal is to force thinking through the design and gather feedback from others for more efficacy. Use this to spell out documentation and systems. Don't try to write this like an academic paper, instead keep it as simple as possible. This doc is to describe your solution and get feedback.  Acheive clarity with simple words, short sentences, bulleted lists, and concrete examples.  

- [] Project Title, Description, purpose and Stakeholders
- [] High-level overview/summary (why project is necessary, how it fits into the technical strategy, product strategy, or the team's quarterly)
- [] Goals & Non-Goals: Impact, metrics (with a dashboard)
- [] What are the user requirements?
- [] What systems will be affected?
- [] What new data structures are needed?
- [] What new APIs are needed?
- [] What are the efficiency considerations (time, space, etc)?
- [] What are the expected access patterns (load/throughput)?
- [] How will data be validated and what are the potential error states?
- [] Are there any logging, monitoring, or observability needs? 
- [] Are there any security considerations?
- [] Are there any privacy considerations?
- [] Are there any mobile consideration?
- [] Are there any web-specific considerations?
- [] How will the changes be tested?
- [] How does internationalization and localization - translations, times zones, unicode, etc. - affect your solution?
- [] Data protection
- [] Existing Solution and current implementation w/ high-level example flow to demonstrate user interaction w/ the system & how data flows through it
- [] Proposed Solution (aka: "Technical Architecture" section)
- [] User Stories for the proposed solution and each of the detail implementations
    - [] big picture first
    - [] fill in lots of details
    - [] high-tech audience
    - [] layman's audience    
- [] List and address any open questions that you're not sure about (aka: "known unknowns")
- [] List any contentious decisions readers should weigh in on
- [] List suggested future work and those details
- [] Detailed Scoping and timeline (at the end of the doc) *(This is used by the engineers, tech leads, and managers for this project.)
- [] Add lots of diagrams and charts (try  Google Drawing) *(Add link to editable version of the diagram under a screenshot for easy updates when things change.)
- [] Include numbers: 
    - [] scale of problem often determines solution.
    - [] real numbers like # of DB rows, # of users, latency
    - [] how the numbers scale with usage (Think Big-O Notation)
- [] Keep it light: have some humor - so its not so boring and you can maintain engagement - but stick to the core idea
    - TIP: Joel Spolsky -'One of the easiest ways to be funny is to be specific when it's not called for {IE:} Instead of saying "special interests," say "left-handed avacado farmers." '
- [] Do the skeptic test: (POV of reviewer - what are ?s and doubts about the design?) - address these premptively.
- [] Do the vacation test: If you go on vacation w/ no internet access, can someone on your team read the doc and implement it as intended? 
- [] Process: write the doc and get feedback from it: DO THIS BEFORE EVEN START WRITING DESIGN DOC for immediate feedback and saves time.  (Also: if implementation stays the same, reviewer is able to point out corner cases needed to be covered, indicate any potential areas of confusion, and anticipate potential difficulties.)
    - [] Everyone working on the project should be par of design process
    - [] Everyone should be involved in discussion and buy into the decision - even if tech leads end up driving a lot of the decisions. (This makes "you" plural - and includes everyone on the project).
    - [] It's ok to just prototype potential solutions - get your hands dirty
        - This is not the same as starting to write production code before writing a design doc (don't do that.) - But DO write hacky throwaway code to validate an idea (make it a rule that non of this code is allowed to be merged to master.)
    - [] Ask an experienced engineer or tech lead on yoru team to be your reviewer.  Ideally this would be someone who's well respected/familiar with the edge cases of the problem. 
    - [] Whiteboard in the conference room
    - [] Describe the problem to the engineer: This is vital step!!
    - [] Explain the implementation in consideration and convince them its the right solution to build. 
    - [] After rough draft of design doc is written - get same reviewer to read through it again, and give stamp of approval of reviewer in Title and Process section of the doc(this creates extra incentive and accountability for the reviewer.)
    - [] consider specialized reviewers (SREs, security engineers, etc.) for specific aspects of the design. 
    - [] upon signoffs, send the design doc to team for additiaonl feedback and knowledge sharing (time-bounding this feeedback gathering process to about 1 week to avoid extended delays.  Commit to addressing all questions and comments people leave within that week.  DO NOT LEAVE COMMENTS UNATTENDED!!![b/c its' super bad!])
    - [] If there is a lot of contention between you, the reviewer, and other engineers reading the doc, consolidate all points of contention in discussion section of the doc. Then, set up meeting with each of the involved parties to discuss disagreements in person.
    - [] If discussion thread is more than 5 comments long, moving to an in-person discussion can be more efficient. (you are responsible for final call - even without consensus.)
    - [] Also, a different engineer on a different team can bring additional insight and feedback (helps improve readability of the doc)


## Third Party Considerations

- [] cost of third party solution (time, money, resources)
- [] scalability (implementation, control, access, cost, maintenance)
- [] Data protection
- [] GDPR - Data processing addendums required?
- [] Collection/Reviews of SOC2 reports?
- [] Notifications of subprocessors, which will affect the roll-out plans

## Cross Team Impact

- [] How will this increase on call and devOps burden?
- [] How much $ will this cost?
- [] Does it cause any latency regression to the system?
- [] Does it expose any security vulnerabilites?
- [] What are some negatives consequences and side effects?
How might the support team communicate this to the customers? 

## Work Estimates

- [] Break down of tasks
- [] Break down of work

## Roll-out plan

- [] Discuss how changes to models and APIs will need to be staged.  
- [] Will you be rolling out incrementally to your users using feature flags?
- [] Discuss the revert path: If something goes wrong, how will you back out partway throught the process while leaving systems in a healthy state?
- [] Identify biggest risks
- [] Spell out how you'll detect and mitigate the above mentioned risks

## Testability, monitoring, and alerting

- [] Implement these from the beginning to the end
- [] These are to save you time, resources, money, and headaches down the road
- [] DO NOT MISS THESE!!!!

## Alternative Approaches

- [] Explain the approaches that were considered and rejected (this saves time from handling rejections for other stakeholders and focus on the design decisions that were chosen.)
- [] Explain why other approaches seemed inferior or wouldn't work.
- [] It's not unusual for info to emerge during design process that escalates an alternative approach to the primary approach.  (If this occurs, try to avoid [sunk cost fallacy](https://en.wikipedia.org/wiki/Sunk_cost).)

## Related work

- [] Are there internal or external projects similar to this project?
- [] Are other teams facing similar challenges?
    - IE: If building your own noSQL DB, this section might include a feature matrix comparing your technical requriements to exiting database offerings.

## Future Work

- [] help prevent bike-shedding and scope creep here.
- [] Identify anything that you're not addressing with this particular design, but should happen in the future or that would be a logical follow-on project
- [] Include a more detailed description of the future goals
- [] Include how some of the non-goals might be addressed in the future

## Implementation

- [] Treat design doc as living documenation as you implement the solution
- [] Update the doc at every new discovery/lesson that triggers changes in the original solution
- [] update scoping as necessary

## Evaluating Success of the design doc

- [] "A design doc is successful if the right ROI of work is done."
- [] Success might look like: 
    - 5 days writing design doc forces you to think through different parts of the technical architecture
    - Getting feedback from reviews that X is the riskiest part fo the proposed architecture
    - Deciding to implement X first to de-risk the project
    - 3 days later - discover X is either not possible or more difficult than anticipated
    - decision to stop working on the project and prioritize other work instead
