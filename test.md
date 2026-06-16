You are a senior solution architect helping me reverse engineer an unsecured loan application flow that starts from a mobile banking app and continues through backend services and downstream banking systems.

Please analyse the provided mobile app code, API contract, backend controller classes, service classes, DTOs, API clients, configuration files, event/message handlers, and any related documentation.

Important rules:

* Do not assume anything that is not supported by the provided code or documents.
* If information is missing, clearly mark it as “not found in provided materials”.
* Do not expose or repeat proprietary names, real API paths, secrets, customer data, internal system names, or confidential implementation details.
* Generalize the final explanation into professional architecture language suitable for an external banking interview.

Please produce the following:

1. Mobile customer journey
    * Identify the user actions in the mobile app.
    * Explain the screen flow, such as loan entry point, eligibility display, application form, confirmation, submission, result page, and status enquiry.
    * Identify what data is collected from the customer and what validation happens on the client side, if visible.
2. Mobile-to-backend API flow
    * Map each mobile screen or user action to the backend API call.
    * Identify request and response objects.
    * Explain how session, authentication, authorization, headers, correlation ID, device/app context, and error handling are passed from mobile to backend, if visible.
3. Backend technical sequence
    * Trace the flow from API gateway or BFF layer to controller, service layer, domain logic, repositories, external clients, and message producers/consumers.
    * Identify the key backend components involved.
    * Explain synchronous and asynchronous steps separately.
4. Lending business flow
    * Explain the end-to-end unsecured loan journey from customer submission to final result or status update.
    * Include eligibility check, offer retrieval, application submission, credit assessment, approval, document handling, disbursement, repayment setup, and status enquiry if found.
    * Clearly mark which steps are confirmed by code and which are not found.
5. Data and status flow
    * Identify important request/response fields, loan application status values, status transitions, and where data is persisted or retrieved.
    * Explain how duplicate submission, resubmission, pending status, rejection, approval, timeout, or partial failure are handled if visible.
6. Downstream integration points
    * Identify external or downstream systems involved, but generalize their names.
    * Explain the purpose of each integration, such as customer profile, credit assessment, loan offer, document service, notification, core banking, payment/disbursement, audit, or reporting.
    * Explain whether each integration is synchronous, asynchronous, batch-based, or event-driven if visible.
7. Security and control points
    * Identify authentication, authorization, input validation, encryption, data masking, secrets management, audit logging, access control, maker-checker, and fraud/risk controls if visible.
    * Highlight any sensitive customer or financial data handling.
8. NFR observations
    * Analyse visible non-functional requirements such as performance, scalability, resiliency, observability, auditability, maintainability, and production readiness.
    * Look for timeout, retry, circuit breaker, cache, Kafka/event handling, Redis usage, monitoring, logging, metrics, tracing, alerting, and runbook-related clues.
9. Failure scenarios and recovery
    * Identify how the system handles downstream timeout, validation failure, technical error, duplicate request, partial submission, failed status update, failed notification, retry, dead-letter queue, and manual recovery if visible.
    * Identify what the mobile app shows to the customer in failure or pending scenarios if visible.
10. Interview-ready summary

* Create a concise, non-confidential explanation I can use in an external interview.
* Write it from the perspective of a Tech Lead / Solution Designer.
* Focus on customer journey, API integration, backend architecture, downstream integration, NFRs, security, observability, and production readiness.
* Do not include internal project names, real API endpoints, table names, class names, or proprietary implementation details.

11. Architecture artifacts

* Produce a generalized customer journey summary.
* Produce a generalized component map.
* Produce a generalized sequence flow in text form.
* Produce a list of open questions I should clarify with the team.

