# Importand questions to ask for detailed design:

There is no hard and fast rule on when a spec if appropriate.  It's a function of complexity, certainty, and risk.  

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
- [] How does internationalization and localization - translations, times zones, unicode, etc. - affect you solution?
- [] Data protection


## Third Party Considerations
- [] cost of third party solution (time, money, resources)
- [] scalability (implementation, control, access, cost, maintenance)
- [] Data protection
- [] GDPR - Data processing addendums required?
- [] Collection/Reviews of SOC2 reports?
- [] Notifications of subprocessors, which will affect the roll-out plans

## Work Estimates
- [] Break down of tasks
- [] Break down of work

## Roll-out plan

- [] Discuss how changes to models and APIs will need to be staged.  
- [] Will you be rolling out incrementally to your users using feature flags?
- [] Discuss the revert path: If something goes wrong, how will you back out partway throught the process while leaving systems in a healthy state?
- [] Identify biggest risks
- [] Spell out how you'll detect and mitigate the above mentioned risks

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



## Resources
-[Better Tech Specs to write design docs](https://www.range.co/blog/better-tech-specs)