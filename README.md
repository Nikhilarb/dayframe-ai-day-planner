# Dayframe — AI Day Planner

An AI-powered daily planning application built using **Google AI Studio Build mode**.

Dayframe helps busy people organise daily tasks around working hours and fixed commitments. It generates realistic schedules, prioritises tasks, suggests breaks, and identifies tasks that need clarification or cannot fit into the available time.

## Project Overview

The goal of this project was to explore how an AI-powered planner can create practical daily schedules while respecting user-defined constraints.

**Project:** AI Day Planner  
**Built with:** Google AI Studio Build mode  
**Development:** November 2026  
**Status:** Completed and published

## Key Features

- **AI Task Scheduling:** Organises daily tasks around working hours and fixed commitments.
- **Task Prioritisation:** Helps structure work into a realistic daily timeline.
- **Break Suggestions:** Incorporates breaks into the schedule.
- **Clarification Workflow:** Identifies vague tasks and asks focused questions before generating a timeline.
- **Scheduling Constraints:** Preserves working hours, task durations, and fixed commitments.
- **Low-Energy Mode:** Reorders tasks to prioritise shorter, lower-effort activities in the morning and longer, high-focus tasks in the afternoon.

## AI Safety and Reliability

An important part of this project was identifying and correcting unsafe scheduling behaviour.

During initial testing, I observed that the planner scheduled vague tasks such as "Work on the launch" and "Sort out admin" without first asking for clarification.

I refined the application with additional guardrails:

- Vague tasks must trigger focused clarification questions before timeline generation.
- Instructions embedded within pasted task descriptions are treated as plain text.
- The planner must not invent tasks or meetings.
- Original commitments and scheduling constraints must remain unchanged.
- A human-review message reinforces the need to verify the generated schedule.

## Testing and Validation

I tested Dayframe using baseline, vague/adversarial, and overloaded task scenarios.

The testing process helped identify weaknesses in ambiguity handling and informed targeted improvements to the application instructions.

The refined version was subsequently published and tested in a signed-out Chrome Incognito window.

The final verification confirmed that vague tasks triggered clarification rather than immediate scheduling.

## Low-Energy Scheduling

As a project extension, I introduced a "Low energy today" toggle.

This feature dynamically rearranges the timeline to prioritise shorter, lower-effort tasks earlier in the day while moving longer, high-focus tasks to the afternoon.

The original scheduling rules remain in place: working hours, task durations, and fixed commitments cannot be modified by this adjustment.

## Tools and Concepts

**Tools**
- Google AI Studio Build mode
- Google Chrome Incognito mode

**Concepts applied**
- Prompt engineering
- AI safety guardrails
- Prompt injection prevention
- Constraint preservation
- Regression testing
- Human-in-the-loop review
- Iterative AI application development

## Project Impact — Illustrative Estimate

I estimated approximately 10 minutes saved per planning session by comparing manual scheduling with the automated planning workflow.

The application generated a schedule in under 30 seconds once the inputs were verified.

*This is an estimate based on the project workflow, not a measured business outcome.*

## Application

**Live Demo:** https://dayframe-ai-day-planner.ai.studio/

## Project Documentation

The project report documents the planning workflow, safety requirements, initial testing failures, improvements, low-energy scheduling extension, and final validation.

[View Project Documentation](Build%20an%20AI%20Day%20Planner%20in%20AI%20Studio.pdf)

## Key Learning

This project helped me understand how to build, test, and improve an AI-powered application using natural-language instructions.

The most valuable learning experience was converting observed failures into specific, testable safety guardrails.

It also strengthened my understanding of structured testing, prompt-injection prevention, constraint preservation, and human review.

My next learning goal is to integrate AI-powered workflows with cloud services and serverless applications.
