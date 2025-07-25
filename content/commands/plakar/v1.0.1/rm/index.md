---
date: "2025-06-30T10:10:26Z"
title: rm
summary: "Remove snapshots from a Plakar repository"
---
PLAKAR-RM(1) - General Commands Manual

## NAME

**plakar rm** - Remove snapshots from a Plakar repository

## SYNOPSIS

**plakar rm**
\[**-name**&nbsp;*name*]
\[**-category**&nbsp;*category*]
\[**-environment**&nbsp;*environment*]
\[**-perimeter**&nbsp;*perimeter*]
\[**-job**&nbsp;*job*]
\[**-tag**&nbsp;*tag*]
\[**-latest**]
\[**-before**&nbsp;*date*]
\[**-since**&nbsp;*date*]
\[*snapshotID&nbsp;...*]

## DESCRIPTION

The
**plakar rm**
command deletes snapshots from a Plakar repository.
Snapshots can be filtered for deletion by age, by tag, or by
specifying the snapshot IDs to remove.
If no
*snapshotID*
are provided, either
**-older**
or
**-tag**
must be specified to filter the snapshots to delete.

The arguments are as follows:

**-name** *name*

> Filter snapshots that match
> *name*.

**-category** *category*

> Filter snapshots that match
> *category*.

**-environment** *environment*

> Filter snapshots that match
> *environment*.

**-perimeter** *perimeter*

> Filter snapshots that match
> *perimeter*.

**-job** *job*

> Filter snapshots that match
> *job*.

**-tag** *tag*

> Filter snapshots that match
> *tag*.

**-latest**

> Filter latest snapshot matching filters.

**-before** *date*

> Filter snapshots matching filters and older than the specified date.
> Accepted formats include relative durations
> (e.g. 2d for two days, 1w for one week)
> or specific dates in various formats
> (e.g. 2006-01-02 15:04:05).

**-since** *date*

> Filter snapshots matching filters and created since the specified date,
> included.
> Accepted formats include relative durations
> (e.g. 2d for two days, 1w for one week)
> or specific dates in various formats
> (e.g. 2006-01-02 15:04:05).

## EXAMPLES

Remove a specific snapshot by ID:

	$ plakar rm abc123

Remove snapshots older than 30 days:

	$ plakar rm -before 30d

Remove snapshots with a specific tag:

	$ plakar rm -tag daily-backup

Remove snapshots older than 1 year with a specific tag:

	$ plakar rm -before 1y -tag daily-backup

## DIAGNOSTICS

The **plakar rm** utility exits&#160;0 on success, and&#160;&gt;0 if an error occurs.

0

> Command completed successfully.

&gt;0

> An error occurred, such as invalid date format or failure to delete a
> snapshot.

## SEE ALSO

[plakar(1)](../plakar/),
[plakar-backup(1)](../backup/)

Plakar - March 3, 2025
