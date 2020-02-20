***************************
Social Capital Requirements
***************************

Social Capital is an Inventory App
==================================

In Social Capital, inventory is a list of your private and shared capital. Capital in the sense of
an inventory of tools and resources that you use to create things. By tracking your inventory in
this app, you can track and record the items you use for your projects. Also you can request and
receive loans of inventory from your sharing networks.


How Do You Record your Inventory Items?
=======================================

To inventory an item, do any of the following **activities**:

.. note:: .item.photos Take a clear set of pictures of an item with your phone

.. note:: .item.product Tag them in your email receipts in order to pick up item PLU information and
	  cost.

.. note:: .item.forms Fill out form(s) in order to update or fill out any of the above fields for an
          item.


What Do You Do With Your Inventory of Items?
============================================

You view and modify inventoried item's schedules. Time records are modified by opening new
activities, or changing the state of activities you have opened.


How Do You View Inventory?
==========================

- email calendars - including email reminders and recurring events. (Idea -- reverse
  exponential-window reminders)
- logs - objective is to form audit trail of all completed transactions where it's possible to
  rollback current state based on merging a networks logs. (Can track expected vs actual inventory
  that way -- good for sub-scheduling situations where someone loans out an item they have on loan).
- csv's
- app dashboads


What is an activity?
====================

Long term, it is an as-run (or running) record with internal state.

Activities are principally run through app prompts. They record a journal of as-executed tasks.

***********
Definitions
***********

.. glossary::

   time_record
      a typed json record, committed to a record_id file location. the file path specifies the
      instantiation ID and record type.

   git_time
      Incorporating metadata into git commits in order to:

      1. track a history of activities (via commit history behind master_HEAD).
      2. track currently running activities (via commit data for all commits that directly branch off
	 master HEAD).
      3. track planned activities (via any commits on those branches thereafter).

      Updating current activities involves updating master head -- which requires planned activities
      to rebase.

   format as calendar
      a git time repo should be formattable as a set of calandar appointment records that when
      viewed, show the past and planned status of each tracked activities and inventoried item in
      <TBD> calendar application.

   format as log
      A git_time repo should be formattable into a debug log: showing a chronology of activity and
      item change records.


