# Zenflow

**A deadline-driven calendar that schedules your study work for you — then learns
how you actually work and personalises itself over time.**

You tell Zenflow *what* needs doing — a study **task** with a duration and a
deadline, or a fixed **lecture / exam / assignment / do-not-disturb** block — and
Zenflow decides *when*. The scheduler drops each new task into its single best
free 15-minute slot before the deadline, scored by a per-student time-of-day
preference. Fixed sessions stay where you put them. Every time you drag or resize
a placed task, that edit becomes a training signal.

## What it does

- **Automatic placement.** An Earliest-Deadline-First core places tasks into open
  slots across your whole calendar — no manual tetris.
- **Learns your rhythm.** A preference heuristic today, and a per-student
  contextual bandit (LinUCB) running as a live A/B experiment, nudge future
  placements toward the times of day you actually keep.
- **University sync.** Connect your Moodle **LMS** and **student portal** and your
  assignment deadlines, weekly timetable and exam schedule land on the calendar
  automatically, kept in sync as rooms and times change — with an in-app
  notification inbox.
- **One calendar, two clients.** A React web PWA and an Expo (iOS / Android)
  app, both speaking the same API.

## Repositories

| Repo | What it is |
| ---- | ---------- |
| [`zenflow`](https://github.com/tryzenflow/zenflow) | The monorepo — web PWA, mobile app, NestJS API + scheduler, shared packages, and the FastAPI bandit service. |

## Status

Early development. The scheduler's preference heuristic and the LinUCB A/B path
are both shipped; DLU ingestion and cross-client parity are in active work.
