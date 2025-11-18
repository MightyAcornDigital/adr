Architectural Decision Record
=============================

This repository contains a template for documenting Architectural Decision Records (ADRs). ADRs are a way to capture important architectural decisions made during the development of a software project.

## What is an Architectural Decision Record (ADR)?

An Architectural Decision Record (ADR) is a document that captures an important architectural decision made along with its context and consequences. ADRs are typically stored in a version-controlled repository alongside the project's source code, making them easily accessible to all team members. They also typically go through a formal review process, although this is often the same as the code review process used by the team.

## Purpose

Architectural decisions can have a significant impact on the success of a project. Taking the time to document these decisions helps to ensure that they are well-thought-out and can be communicated effectively to all stakeholders. The practice of writing and reviewing ADRs encourages a more deliberate approach to important technical decisions, leading to better outcomes. It also preserves the context and reasoning behind decisions, which is helpful for future maintenance and development.

## What kinds of decisions should be documented?

Ultimately, this decision is contextual to the team and project, but as a rule of thumb, consider an ADR for decisions that:

* Might be controversial.
* Have multiple viable options.
* Involve significant trade-offs.
* Will have a long-term impact on the system.

## What goes into an ADR?

Glad you asked! There are a lot of different templates you can use for this, but we've found that the most important info is captured in the template in this repository.

To create an ADR, simply copy the template file, rename it to ([DATE]-[TITLE].md), and fill in the sections. For example, if you made a decision on June 1, 2024, to use PostgreSQL as your database, you might name the file `2024-06-01-use-postgresql.md`. ADRs are typically stored in the `docs/decisions/` directory of a project.
