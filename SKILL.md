---
name: ui-principles
description: 18 numbered design principles that decide what goes on a screen, how it behaves, and how it looks. Use when designing or building a surface or control, when reviewing or critiquing an interface, or when choosing between two UI options.
---

# UI principles

18 principles, numbered so a review can point at one. They decide what goes
on a screen, how it behaves and how it looks — a standard to decide by, not
a checklist to cite.

Applies to any interface a person operates to get work done, repeatedly: an
app, an editor, a plugin, a tool, a terminal program. Repeat use is the
assumption behind 5 and 13. Accessibility, keyboard handling and visual
values live in their own documents. The examples assume a pointer; on a
terminal, touch or voice host, keep the principle and substitute the
mechanism.

Two words used throughout. **Host**: whatever the tool lives in — the OS,
the application it plugs into, the browser, the terminal. **Medium**: what
the user is producing — audio, pixels, text, data.

## Working to these

- **Designing.** Start from the decisions (4): list what the user decides on
  this surface and how often, before writing any layout. Compose from that
  list, not from the screens that already exist.
- **Checking.** Run the result against the principles before calling it
  done. 7, 8 and 11 are the ones a plausible-looking control breaks
  silently.
- **Reviewing.** Cite the number: "this breaks 13" is a decision, "this
  feels wrong" is not.
- **On a conflict.** Choose one and name the one you gave up. Trading 11 for
  10 is a decision, not a violation.

## Philosophy

**1. Less is more.** The UI is just a tool; the ideal UI is no UI, and the
tool disappears into the task. If skipping a whole workflow gives the user a
better result, skip it. Simplify wherever the user gains from it. Every
element earns its place by serving a real purpose; nothing repeats what is
already visible. Make users think less: fewest steps, not fewest elements.
Each fact has one home: a state is said once, where it belongs, and not
echoed elsewhere. Marks are for exceptions: a step or change that went as
expected carries none.

**2. Implicit over explicit.** Users are smart; they discover how things
work. The mechanics of the app stay transparent: the user does their work
and never cancels one thing to start another. The flow is continuous.
Explanations appear on demand, never up front. Implicit applies to
explanations, never to affordances: the options of the core decision are
always visible where the user makes it. Work happens inline; a modal is the
last resort. A tooltip tells what can't be seen: the name of an icon-only
control, why something is unavailable, or text cut short. It never repeats a
visible label or teaches a standard gesture.

**3. Piano, not saxophone.** Approachable at first touch, deep on demand.
Core things sit in front; sophisticated ones wait behind an interaction, a
context or a mode. Emphasis is scarce: one primary action, accent colour
only for action, selection and state. Tone sits on neutral: an error or
notice keeps a neutral surface; only its icon and headline carry the colour.

**4. Start from the decisions.** Before any layout, list the decisions the
user makes and how often each one happens. The frequent decision gets the
most direct, visible gesture; rare edits stay available but out of the way.
An option is labelled by its outcome, the value it produces, not by the
mechanism: "Delete 12 files", not "Apply cleanup".

**5. Optimize for utility.** Judge a design by the effort the work takes,
not by how few elements it has. Find the action the user repeats most and
make it the cheapest: one fixed target, no reaching, no aiming. An element
that removes repeated effort has earned its place (1).

## Behaviour

**6. Direct manipulation.** The user acts on the object itself, where it is
shown. No form or dialog stands between the user and the object.

**7. One gesture, one meaning.** Each surface and each gesture does exactly
one job. Navigating, structuring and choosing never share a gesture; a
gesture commits one decision. Hover informs, click acts: nothing audible or
stateful happens on hover. Follow the host's learned mappings: the thing you
navigate is the thing you see, and edits happen where the focus is. A row is
either one target or a holder of its own controls, never both. A glyph means
one thing everywhere: × closes and never deletes; the trash deletes. A mode
offers only its own actions: an editor has Save and Cancel, nothing else.

**8. Only valid controls.** A control exists only if every value it can
reach is valid in the workflow. What the system fixes is shown, not offered.

**9. Judge by the medium.** Judge the result through the channel the work
lives in: for audio, listening; for images, the pixels; for text, how it
reads. Everything else serves that channel: switching is instant and
uninterrupted, and the medium never stops so the interface can catch up.

**10. Instant.** Every action shows its result at once. Sync happens out of
sight, and a late update never reverses what the user just did; the source
of truth — the file, the server, the host — has the final word on the actual
state. What is shown and what is happening never diverge: this one is
non-negotiable.

**11. Never in the way.** Nothing blocks the user's workflow unless the
block is critical to that workflow. A wait affects only what is actually
waiting; everything else keeps working. Short waits stay invisible; long
ones show where they happen. Controls are welcoming. An action stays enabled
when input is missing; pressed, it harms nothing and says what's missing,
next to it. A control is disabled only for a reason outside the user's
input, and it says that reason.

**12. Show what changed.** Show the difference, not the whole state: what is
new, what it was before, and who made it — the tool, the user, or an
upstream source. The user's own edits outrank the tool's and are never
silently overwritten.

**13. Safe to try, nothing lost.** Exploring costs nothing: the original is
always kept, every change can be undone, temporary changes are cleaned up.
Undo, not confirm: a removal happens at once, and the one offer to undo it
appears quietly in the status line, never as a row in the content. What the
user typed, where they are and what they were looking at survive switching,
errors and coming back. Confirmation is asked only when an action reaches
beyond what the user can see.

## Look and feel

**14. One vocabulary.** The same thing looks and behaves the same way
everywhere. The material says what you can do: editable text sits in a
field, an action is a filled control, a card is only a surface. One type
family; monospace only for literal text the user may copy. One motion, one
tooltip, one menu, shared by every surface.

**15. Crafted.** Native-platform fluidity, motion, interactivity and polish.
Motion is short, interruptible and shows a change of state, never
decoration. Whatever arrives, changes or leaves moves like a disclosure
opening: nothing pops in, nothing below it jumps. Layout stays still under
the user's attention; nothing moves under the pointer, and a state that
comes and goes shares a slot with one that stays, so text never shifts. No
state is left undesigned: empty, busy, error and disabled get the same care
as the main state; disabled keeps its shape and fades, it doesn't turn into
an outline.

**16. Gestalt.** Things that belong together stay together and look alike;
unrelated things are not grouped. Proximity, similarity and enclosure show
how things relate, so the layout explains itself. The layout mirrors the
model: the structure of the decision is the structure of the screen. A
control sits next to what it acts on, on its first line, never in a detached
column.

**17. At home in the host.** Native polish in feel, the host's own
conventions for gestures, modifiers and theme. Familiar controls over
invented ones. Buttons follow the platform's order: on Windows the primary
first, then Cancel; on macOS Cancel, then the primary at the right, with a
destructive choice set apart on the left.

**18. Precise.** Alignment is optical and nested corners are concentric. The
focus ring is for the keyboard, never left by a click. Design for the
longest string and the right reader: labels wrap rather than compete, and a
surface for reviewing is sized for reading.
