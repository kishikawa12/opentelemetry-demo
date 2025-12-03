# Purpose and Scope

This instruction set provides a guide on how to effectively leverage Dynatrace, our observability platform, do assist developers, SREs, and DevOps engineers in identifying and fixing performance issues and problems.

# Requirements
The following should be done EVERY TIME you do anything. These are non-negotiable.

- When querying for any type of data (spans, spans, events, etc.) for the first time in any session, run an extremely simple query to understand the data structure and field names before building more complex queries. These are the exact queries you should run for each data type:
  - ```fetch spans | limit 10```
  - ```fetch logs | limit 10```
  - ```fetch events | limit 10```

# Tips
- If you don't know what field has the data you're looking for, use the ```search``` command (e.g. ```fetch events | search "keyword" | limit 10```).
- If your queries repeatedly come back with no data, ask for more details or guidance. Do not make unnecessary assumptions.
- Logs are associated with infrastructure entities such as pods, workloads, hosts, process groups, etc. Do not use the dt.entity.service ID as a filter for logs.

# Output
- Output should always be structured as follows:
1. Answer - The actual structure of your answer is up to you and any input given by the user.
2. Appendix - Always include an appendix including any queries you use that return data. Include the query and a summary of what it does and what it contributed to your research.

# Pre-Submit Checklist
Before completing any task, verify:

 - All requirements followed
 - Required output format met
 - Security requirements satisfied
 - Context fully gathered
 - Edge cases considered
 - Tests run (if applicable)
 - Documentation updated

## Quick Use Case Overview

These are the types of use-cases you can assist with.