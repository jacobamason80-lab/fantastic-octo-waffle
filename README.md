ERD Design Report: Customer Help Desk System
1. Fields Added and Why They Are Critical
For the Customers table, I added full_name, account_created_date, and status to clearly identify users,
track account age, and indicate whether an account is active or suspended. For the Support Agents
table, I added agent_name, shift, and active_flag to support staffing analysis and prevent tickets from
being assigned to inactive agents. For the Support Tickets table, I added status, priority, subject,
description, resolution_code, and resolved_date to track ticket lifecycle, urgency, context, and final
outcomes.
2. Changes to Provided Fields
No provided fields were removed because each one supports realistic help desk operations and
reporting. Customer_tier was kept because it affects service levels and escalation rules. Team and
skill_level were kept to explain ticket assignment patterns. Issue_category was kept because it
provides an initial classification for routing and reporting, even though deeper analysis relies on
additional fields.
3. Most Important Field for Root Cause Analysis
The most important field for root cause analysis is resolution_code. While issue categories are often
broad, resolution codes capture the actual cause or fix, such as a system outage or billing error. When
many tickets share the same resolution code, recurring problems can be identified. This makes
analytics and future AI insights more accurate and actionable.
4. Most Important Field for Measuring Support Performance
The most important field for measuring support performance is resolved_date when paired with
created_date. These two fields allow the organization to calculate resolution time, which is a key
performance metric. Without accurate resolution timestamps, it is difficult to evaluate agent efficiency or
meet service-level agreements. Time-based metrics are essential for fair performance tracking.
5. Problems Caused by Inconsistent Issue Categories or Status Values
If issue_category or status values are inconsistent, AI models and reports become unreliable. Similar
problems may be labeled in different ways, making trend detection inaccurate. Inconsistent status
values can also break lifecycle reporting and confuse predictive models. Clean and consistent data is
critical for trustworthy AI-driven insights.
