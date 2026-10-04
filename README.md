# PF2e Fling Magic

## Purpose and features

Fling Magic adds castable spell cards for the Thaumaturge's Fling Magic ability. It provides normal and Boosted cantrips with only the elements the character has earned, and applies the Adept or Paragon elemental rider after a failed save.

## Setup

The manifest supports Foundry VTT 12 or later and PF2e 6.0.0 or later; it was verified on Foundry VTT 14 with PF2e 8.5.0.

This is a free module. Install it with the [SpazzMods Installer](https://github.com/Spazzletopia-Studios/spazzmods-installer/releases/latest), or use the [public GitHub release](https://github.com/Spazzletopia-Studios/pf2e-fling-magic/releases/latest). Enable **PF2e Fling Magic** in Manage Modules.

## Quick start

1. Open an eligible Thaumaturge character sheet.
2. With Hub enabled, open the SpazzMods dropdown in the sheet header and choose **Configure Fling Magic**. Without Hub, use the original **Configure Fling Magic** header action.
3. Choose the number of elements shown for the character's level: one at level 1, two at level 7, or three at level 17.
4. Choose **Save and Install Cards**.
5. Cast either Fling Magic cantrip from the character's spell list.

## Detailed use

The module creates a managed innate spellcasting entry if the actor does not already have one. It installs the normal and Boosted Fling Magic cards from its **Fling Magic Cantrips** pack. The cards use the Thaumaturge class DC and PF2e's normal basic Reflex save and damage flow.

A failed save at Adept or Paragon applies the selected element's rider: Fire deals persistent damage, Cold reduces Speed for one round, and Electricity grants its effect for one round. The rider uses the tier stored on the cast card, so leveling up does not change an older card. A rerolled save replaces the earlier rider.

**Boosted** is a separate card. Follow the feat's once-per-round extra-energy rule; the module does not choose when to spend it. If the character levels up or changes their earned elements, run setup again to update the cards.

## Settings

No configurable module settings are registered. Choose the earned elements from **Configure Fling Magic**.

## Limits and recovery

The setup requires the Fling Magic action on a character or a recognized Fling Magic card. If the compendium pack is missing, restart Foundry and try again. The source items and spells remain unchanged; only module-managed Fling Magic cards and their innate entry are maintained.

## Development

The API is `game.pf2eFlingMagic`: `configure(actor)` opens the element setup, `elements(actor)` returns the saved choices, and `tier(actor)` returns the tier for that actor.

The module's source checks are in `harness/`. Run the documented harness commands from that folder. A source gate does not replace an installed Foundry smoke.

## Credits and license

Author: Spazzledorf. MIT License.

## Get help

[SpazzMods Support](https://github.com/Spazzletopia-Studios/spazzmods-support).
