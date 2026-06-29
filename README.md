# Volunteer Data Cleaner

A Python script that takes a messy volunteer sign-up spreadsheet and turns it
into a clean list plus a quick summary of total volunteer hours.

## What it does
Nonprofit volunteer exports are usually messy — duplicate sign-ups, names typed
different ways, dates in three different formats, blank cells. This script cleans
all of that up and then answers a basic question the organization actually cares
about: how many volunteers do we have and how many total hours did they give?

On the test data it took 10 messy rows down to 6 real volunteers and reported
26 total hours, averaging 4.3 hours per person, with a per-day signup count.

## How I built it
- Google Colab (Python in the browser, nothing to install)
- Python with the pandas library
- I used Claude to help write the code, but made the judgment calls myself —
  for example, deduplicating by email instead of by name (since names were typed
  inconsistently but email is the reliable fingerprint of a person), and choosing
  to keep volunteers who logged hours but had no email on file, rather than
  deleting them. They still did the work.

## Who it helps
The person running a small organization. Cleaning a volunteer sheet by hand is
slow and error-prone — this automates that step so they can spend their time on
the volunteers, not the spreadsheet.

## What I'd add next
Pull in volunteer phone numbers alongside the emails, so the cleaned list is
also a usable contact sheet for reaching people directly, not just a record of
hours.
