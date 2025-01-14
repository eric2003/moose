# {{project}} System Requirements Specification

## Introduction id=introduction

### System Purpose id=system-purpose

!template field key=system-purpose
Summarize the reason(s) for the system being developed or modified.

### System Scope id=system-scope

!template! field key=system-scope

Delineate the following:

1. Identify the product(s) to be produced by name (Network Infrastructure, Host DBMS, Report
   Generator, HPC Server, etc.)
1. Explain what the product(s) will, and, if necessary, will not do.
1. Describe the application of the  product being specified, including relevant benefits,
   objectives, and goals.

!alert note
Be consistent with similar statements in higher level specifications (e.g., business requirements
specification).

!template-end!


## System Overview id=system-overview

### System Context id=system-context

!template field key=system-context
Describe at a general level the major elements of the system including user roles and how they
interact. The system overview includes appropriate diagrams and narrative to provide the context of
the system, defining all significant interfaces crossing the system's boundaries.

### System Functions id=system-functions

!template! field key=system-functions
Provide a summary of the major use cases or functions, conditions, and constraints. For example, a
specification for an accounting program may use this part to address customer account maintenance,
customer statement, and invoice preparation without mentioning the vast amount of detail that each of
those functions requires.  Sometimes the function summary that is necessary for this part can be
taken directly from the section of the higher-level specification (if one exists) that allocates
particular functions to the product. Note that for the sake of clarity:

1. The functions should be organized in a way that makes the list of functions understandable to the
   customer or to anyone else reading the document for the first time.
2. Textual or graphical methods can be used to show the different functions and their
   relationships. Such a diagram is not intended to show a design of a product, but simply shows the
   logical relationships among variables.

#### Example

+Use Case+: Submit Timesheet

+Brief Description+: The Employee enters hourly data for the week and submits for approval.

+Initial Step-By-Step Description+:

Before entering their timesheet, the employee must select the "ETS" or "ETS with Login Prompt" menu
option from Nucleus and be logged into the Human Resource application.

1. The system presents the timesheet data entry interface to the employee with any previously saved
   data.
2. The employee enters charge No., TRC, and hours for each work day.
3. The employee may click "Save for Later," exit, and return at a later time to complete timesheet OR
   the employee may click "Submit" to submit timesheet.
4. Following submittal, the system verifies the information (e.g., 40 hours). If information is not
   correct or complete, the employee will receive a warning; otherwise, the employee will be provided
   a confirmation that the time sheet was submitted with date and time.

!template-end!


### User Characteristics id=user-characteristics

!template field key=user-characteristics
Identify each type of user/operator/maintainer of the system (by function, location, type of device),
the number in each group, and the nature of their use of the system.


### Assumptions and Dependencies id=assumptions-and-dependencies

!template field key=assumptions-and-dependencies
List each of the factors that affect the requirements and should be taken into consideration for
derivation of lower level requirements and design. These factors should include design inputs, design
constraints, and installation considerations. Changes to these can affect the requirements in the
specification. For example, an assumption may be that a specific operating system will be available
on the hardware designated for the product. If, in fact, the operating system is not available, the
specification would then have to change accordingly.


## References id=references

!bibtex bibliography title=None


## Definitions and Acronyms id=definitions-and-acronyms

!template field key=definitions-and-acronyms
This section defines, or provides the definition of, all terms and acronyms required to properly
understand this specification.


### Definitions id=definitions

!template! field key=definitions
Add or revise spcific defintions.

- +Baseline+: A specification or product (e.g., project plan, maintenance and operations (M&O) plan,
  requirements, or design) that has been formally reviewed and agreed upon, that thereafter serves as
  the basis for use and further development, and that can be changed only by using an approved change
  control process [!citep](ASME-NQA-1-2008).

- +Validation+: Confirmation, through the provision of objective evidence (e.g., acceptance test),
  that the requirements for a specific intended use or application have been fulfilled
  [!citep](ISO-systems-software).

- +Verification+: (1) The process of: evaluating a system or component to determine whether the
  products of a given development phase satisfy the conditions imposed at the start of that
  phase. (2) Formal proof of program correctness (e.g., requirements, design, implementation reviews,
  system tests) [!citep](ISO-systems-software).

!template-end!


### Acronyms id=acronyms

!template! field key=acronyms
Define specific acronyms.

| Acronym | Description |
| - | - |
| ASME | American Society of Mechanical Engineers |
| DOE | Department of Energy |

!template-end!


## System Requirements id=system-requirements

!template field key=system-requirements required=False

!template! field key=minimum-requirements

For software projects, the following is required:

1. The software requirements shall include technical requirements including operating system,
   function, interfaces, performance, and security requirements, installation considerations, design
   inputs, and any design constraints.
1. Identify applicable reference drawings, specifications, codes, standards, regulations, procedures,
   or instructions that establish software requirement test, inspection, and acceptance criteria.
1. Software requirements shall be traceable throughout the life cycle.
1. Security requirements shall be specified commensurate with the risk from unauthorized access or
   use.

!template-end!

### Functional Requirements id=functional-requirements

!template! field key=functional-requirements
This section of the specification should contain all of the use cases or functional requirements to a
level of detail sufficient to enable designers to design a system to satisfy those requirements, and
testers to test that the system satisfies those requirements.

1. Functional requirements must be stated in form to be:

   - correct,
   - unambiguous,
   - complete,
   - consistent,
   - verifiable, and
   - traceable.

1. Functional requirements should be cross-referenced to earlier documents
   that relate (e.g., business requirements).
3. Functional requirements should be uniquely identifiable.
4. Careful attention should be given to organizing the requirements to maximize readability.

List each function and its defining requirements here. For each function that is defined, one or more
requirements are then described that define the functionality. The requirements should be as
objective and measurable as possible.  Use one of the following examples as a guide for formatting
the requirements.

!template-end!

!template! field
      key=useability-requirements
!template field-begin
## Usability Requirements

Define usability requirements. Usability requirements and objectives for the system or service
include measurable effectiveness, efficiency, and satisfaction criteria in specific contexts of
use. For example:

| Number | Requirement Description |
| - | - |
| U1.1 | Users shall be able to point-and-click a date rather than typing a date into a text field or selecting month, day, and year independently. |
| U1.2 | Users shall select values from a list of valid values instead of having to type a value into a text field |

!template-end!


### Performace Requirements id=performance-requirements

!template! field key=performance-requirements
Define the critical performance conditions and their associated capabilities by including such
considerations as:

1. Dynamic actions or changes that occur (e.g., rates, velocities, movements, and noise levels).
1. Quantitative criteria covering endurance capabilities of the equipment required to meet the user
   needs under stipulated environmental and other conditions, including minimum total life
   expectancy. Indicate required operational session duration and planned utilization rate.
1. Performance requirements for the operational phases and modes.
1. To assess the performance of a system, response time, workload, scalability, and platform should
   be addressed.

For example:

| Number | Requirement Description |
| - | - |
| P1.1 | The timesheet application shall be capable of supporting at least 2,500 concurrent users. |
| P1.2 | Visible pages shall respond in 2 seconds or less. |
| P1.3 | Timesheet submittal shall respond in 8 seconds or less. |

!template-end!


### System Interfaces id=system-interfaces

!template! field key=system-interfaces

Specify requirements for interfaces among system elements and with external entities. Interfaces
among system elements should include interfaces with the human element. Interfaces with external
entities should include other systems.  Define any interdependencies or constraints associated with
the interfaces (e.g., communication protocols, special devices, standards, fixed formats). Each
interface may represent a bidirectional flow of information.

!alert note
A graphic representation of the interfaces can be used when appropriate for the sake of clarity.]

| Number | Requirement Description |
| - | - |
| SI1.1 | The timesheet application shall interface with Asset Suite---Accounts Payable. |

!template-end!

### System Operations id=system-operations

#### Human System Integration Requirements id=human-system-integration

!template! field key=human-system-integration
Reference applicable documents and specify any special or unique requirements (e.g., constraints on
allocation of functions to personnel and communications and personnel/equipment interactions). This
should include accessibility requirements related to the ability of disabled individuals to access
the information or service provided by the system.

Define any specific areas, stations, or equipment that would require concentrated human engineering
attention due to the sensitivity of the operation or criticality of the task (i.e., those areas where
the effects of human error would be particularly serious).
!template-end!

#### Maintainablity id=maintainability

!template! field key=maintainability
Specify the quantitative maintainability requirements that apply to maintenance in the planned
maintenance and support environment. Examples are as follows:

1. Time (e.g., mean and maximum downtime, reaction time, turnaround time, mean and maximum times to
   repair, mean time between maintenance actions).
1. Rate (e.g., maintenance staff hours per specific maintenance action, operational ready rate,
   maintenance time per operating hour, frequency of preventative maintenance).
1. Maintenance complexity (e.g., number of people and skill levels, variety of support equipment,
   removing/replacing/repairing components).
1. Maintenance action indices (e.g., maintenance costs per operating hour, staff hours per overhaul).
1. Accessibility to components within systems and to parts within components.

!template-end!

#### Reliability id=reliability

!template field key=reliability
Specify the system reliability requirements in quantitative terms, including the conditions under
which the reliability requirements are to be met. This may also include the reliability apportionment
model to support allocation of reliability values assigned to system functions for their share in
achieving desired system reliability.

### System Modes and States

!template! field key=system-modes
If the system can exist in various modes or states define these and, as appropriate, use diagrams.

!alert note
The mode of a system refers to a collection of states.
!template-end!

### Phyisical Characteristics

!template field key=physical-characteristics
Include constraints on weight, volume and dimension. Include the construction characteristics of
where the system will be installed, requirements for materials to be used in the item or service
covered by this specification, and requirements covering nameplates and system markings,
interchangeability of equipment, and workmanship.

### Environmental Conditions

!template field key=environmental-conditions
Include environmental conditions to be encountered by the system. The following areas should be
addressed: natural environment (e.g., wind, rain, temperature, flora, fauna, fungus, mold, sand, salt
spray, dust, radiation, chemical, and immersion); induced environment (e.g., motion, shock, noise,
electromagnetic, thermal); electromagnetic signal environment; self-induced environment (e.g.,
motion, shock, noise, electromagnetic, thermal); threat; and cooperative environment. Consideration
should also be given to legal/regulatory, political, economic, social, and business environment.

### System Security

!template field key=system-security
Define the system security requirements related to the environment that houses the system and
operational security requirements of the system itself. Examples of such requirements are data
privacy, user access, user privilege, export control, system configuration, event logging and
communications.

### Information Management

!template field key=information-management
Define the requirements for the system's management of information that it receives, generates, or
exports. Examples include types and amounts of information the system is required to receive and
store, any proprietary or other protections levied on the information the system deals with, and what
backup and archiving requirements exist for the information.

### Polices and Regulations

!template! field key=policies-and-regulations
Detail any relevant organizational policies that will affect the operation or performance of the
system as well as any relevant external regulatory requirements, or constraints imposed by normal
business practices. Examples of requirements include multilingual support, labor policies, protection
of personnel information, and reports to a regulatory agency.

Specify health and safety criteria, including those basic to the design of the system, with respect
to equipment characteristics, methods of operation, and environmental influences such as toxic
systems and electromagnetic radiation.
!template-end!

### System Life Cycle Sustainment

!template field key=system-life-cycle
Outline quality activities, such as review, and measurement collection and analysis, to help realize
a quality system. Life cycle sustainment also includes provision of facilities needed to provide
operational- and depot-level support, spares, sourcing and supply, provisioning, technical
documentation and data, support-personnel training, initial cadre training, and initial
contractor-logistics support.

### Packaging, Handling, Shipping and Transportation

!template field key=packaging
Define requirements imposed on the system to ensure that it can be packaged, handled, shipped, and
transported within its intended operational context.


## Verification

!template field key=verification
Provide the verification approaches and methods planned to qualify the system or system element. The
information items for verification are recommended to be given in a parallel manner with the
information items in Subsections 3.1 through 3.13.
