# Team Project - XXX - Enterprise Architecture Modelling

The original assignment and case description is [here](https://docs.google.com/document/d/13vUmeWuM2COGP6vKGhU66AC_evl0T1YajcbFQybSm5Q/edit).

### 0. Preface.

#### What are we going to do?
1. Define the mission of the company.
2. Define the CSF - the company's mission becomes impossible without them - the cause of the company's success.
3. Performance Prism
4. Define the KPIs - what indicates that the company is winning

### 1. Business profile - general
**Name**: New Century Wellness Group

**Address**: Brea, California

**Status**: live company

**Contact**: Dr. Jones, Dr. Garcia, Lisa Sung

**Partners/managers**: Dr. Jones, Dr. Garcia

**Year established**: 5 years ago

**Capital managed**: n/a, additional information is needed

**Industry preferences**: preventive medicine and traditional medical care

**Current permanent staff**: at least 17 (mentioned in the document), 21 according to the book

**Number of customers**: 3500 patients,  275 employers

**Competitors**: The clinic has competition from other health care providers, but no other clinic offers the same range of services.

We have rethought the New Century Wellness Group in order to make it fit better into our Big Data Systems program.

We've made the following suggestions:
- New Century Wellness Group is still a small company but they want to scale and widen the range of their clients
- They want to increase the level of their non-medical services
- They want to suggest their customers a new service - support in workplace programs implementation


### 2. Mission
- to promote and support programs that encourage the wellness of our clients' employees through education and initiatives that:
  - Encourage habits of wellness
  - Increase awareness of factors and resources contributing to well-being
  - Inspire and empower individuals to take responsibility for their own health
  - Support a sense of community
-  to support the adoption of attitudes that contribute to positive well-being and providing information, activities and services designed to support healthy lifestyle choices.

### 3. Goals
![Goal tree img][goal-tree]

### 4. Critical Success Factors
Based on the mission of the company we can determine the CSF<sup>1</sup>:
- Clients' executives sponsorship and visible support
- Embedded in organization’s strategic direction and frameworks
- Measurement - baseline and ongoing
- Program alignment with demographic profile, needs and interests of customers population
- Effective marketing services to companies and individuals
- Recruitment of experienced managerial talent
- Clients accessibility
- Dedication and hard work of the founders
- Raising productivity
- Lowering overall costs
- Medical supplies quality
- Medical supply deliverance accuracy

#### 5. The Performance Prism <sup>2</sup>

![pp](https://github.com/BigDataHSE2016/m01-02-sa/blob/master/m02-gr-prj/team-xxx/perf-pr.png?raw=true)

##### Stakeholder satisfaction
Who are our stakeholders? | What do they want?
--- | ---
Investors | a return on their investment in the form of capital gains, reward for loyalty in the form of dividends or interest
Investors | accurate results and reports from the organisation
Investors | faith in the management team
Customers | ‘fast, right, cheap and easy’ + confidence + information accessibility
Employees | interesting work, wish to be cared for by their employer, to learn transferable skills and to receive decent level of remuneration
Suppliers | a relationship that allows them to be profitable, and enables their business to grow
Suppliers | receive feedback on their performance
Suppliers | want to be trusted
Regulators | act legal, fair, safe and true

##### Stakeholder contribution
Stakeholder | What do we want and need from them?
--- | ---
Investors | capital for growth
Employees | skill growth, confidence in data, people-based culture
Regulators |  lack of bureaucracy, confidence in data

##### Strategies
(what strategies do we need to put in place to satisfy the wants and needs of or our stakeholders while satisfying our own requirements too)
- create a marketing department
- develop a marketing plan
- develop a promotional campaign framework for implementing into b2b clients' companies (using newsletters, signs, bulletin boards, computers, and other media available within the workplace)
- develop a promotional campaign for attracting and maintaining b2c customers
- proactive availability of information
- promote superiority of core service


##### Processes
(what processes do we need to put in place to enable us to execute our strategies)
Title | Who's responsible | Data required  |  Data generated
--- | --- | --- | ---
Gathering statistics about clients, suppliers and employee | Marketing | Inventory lists, supplies usage records, suppliers info, patients personal and financial data | Statistics
Promo campaign template implementing | Marketing | New b2b customers' data | Documentation
Staff accessment| HR | Staff records old | Staff records new


- customer service strategy
- proactive traces
- customer access tools

Existing ones:
 Title | Who's responsible | Data required  |  Data generated
--- | --- | --- | ---
Medical supplies ordering	| Carla Herrera |	Inventory lists, supplies usage records, suppliers info	| Updated inventory lists, supplies orders and bills
Patient intake |	Lisa Sung	| Doctor availability and patients personal and financial data |	Patients and insurance records; doctors' schedule
Insurance billing	| Tammy Alipio |	Patients personal and financial data, insurance contracts |	Bills sent to insurance companies and patients
Accounts recievable	 | Tom Capaletti |	Payments and invoices |	Accounting data
Payroll	| Corrine Sommers (Fred Brown) | Employee list, pay rates, employee's accounts info, employee's schedules, employee's benefits lists | Payments to the employee, records about these payments
Hiring a new stuff member	| Fred Brown |	New stuff member's personal info |	New payroll, set of benefits

##### Capabilities
(what capabilities do we need to put in place to allow us to operate our processes?)
- teamwork
- technology
- additional fundation/investments
- marketing and IT professionals to join the teamwork
- product offering


#### 6. KPI
Thus the sample KPIs can be suggested:
Title | Rationale | Target  |  Data Source(s) | W
--- | --- | --- | --- | ---
Amount of b2b clients | More companies trust the NCWG => better promotion of wellness | Marketing service | Clients DB | 1/4
AVG % of b2b's employee involved in the program | The wellness community in the company size | Marketing service | Customer surveys | 1/4
AVG % of returning  b2с customers | Wellness community quality | Marketing service | Clients DB, customer surveys | 1/4
Accordance between demographic profile of the design client and a real client | The better we predict the client's profile the more relevant service can be suggested | Marketing service | Client records, surveys | 1/4
Patient Wait Time | --- | Patient intake | Patients records | 1/2
Patient Satisfaction | --- | Patient intake | Patients records | 1/2
Staff turnover | --- | HR | Staff records | 1


#### Organisation structure

<img src='http://g.gravizo.com/g?
@startuml;
usecase dir as "Board:;
--;
Dr.Jones, Dr.Garcia";
usecase found as "CEO:;
--;
Dr.Jones";
usecase office as "Office manager:;
--;
Anita Davenport";
usecase medrec as "Medical records\n maintenance:;
--;
Susan Gifford";
usecase hr as "HR and employee\n benefits:;
--;
Fred Brown";
usecase tax as "Payroll, tax reporting,\n profit; distribution:;
--;
Corinne Summers";
usecase acc as "Accounts recievables:;
--;
Tom Capaletti";
usecase ins as "Insurance billing:;
--;
Tammy Alipio";
usecase app as "Customers support and\n appointments:;
--;
Lisa Sung";
usecase suppl as "Office and medical\n supplies:;
--;
Carla Herrera";
usecase meds as "Med Staff:;
--;
4 doctors\n3 physical therapists\n4 nurses)";
usecase mrkt as "Marketing\nDept";
usecase it as "IT Dept";
dir -down-> found;
found -down-> mrkt;
found -down-> it;
found -down-> office;
office -down-> medrec;
office -down-> hr;
hr -down-> tax;
office -down-> acc;
office -down-> ins;
office -down-> app;
office -down-> suppl;
found -down-> meds;
mrkt -down-> (Marketing\noutsourcing);
it -down-> (IT outsourcing);
@enduml
'>

### 2. Business processes
_Identify six business processes that New Century performs, and explain who has primary responsibility for each process. Construct the Organizational chart structured by department and basic business-processes._

----

**Footnotes:**

1. See Critical success factors (ACCA) in [1](http://www.accaglobal.com/ng/en/student/exam-support-resources/professional-exams-study-resources/p3/technical-articles/critical-success-factors.html)
2. The Performance Prism (ACCA) in [2](http://www.accaglobal.com/caribbean/en/student/exam-support-resources/professional-exams-study-resources/p5/technical-articles/performance-prism.html)

[goal-tree]:
https://github.com/BigDataHSE2016/m01-02-sa/raw/master/m02-gr-prj/team-xxx/goal_tree.png

[swot-img]: https://github.com/BigDataHSE2016/m01-02-sa/raw/master/m02-gr-prj/team-xxx/swot.png

[diag1]: https://github.com/BigDataHSE2016/m01-02-sa/raw/master/m02-gr-prj/team-xxx/diag1.png

[0dfd-img]:
https://github.com/BigDataHSE2016/m01-02-sa/blob/master/m02-gr-prj/team-xxx/0dfd.png?raw=true

[pp-img]:
https://github.com/BigDataHSE2016/m01-02-sa/blob/master/m02-gr-prj/team-xxx/perf-pr.png?raw=true
