# Schichtplaner

Self-contained HTML tool for generating a Schicht- und Urlaubsplan (shift & vacation calendar) for a 6-team continuous shift rotation.

## Usage

Open `index.html` in any browser (no server, no build step, no dependencies). Everything runs client-side.

You can configure:

- **Schicht-Rhythmus**: the repeating F/S/N/A/U/- shift pattern and its start date
- **Schicht-Auswahl**: which of the 6 rotating teams (Gelb/Blau/Rot/Grün/Braun/Schwarz) the plan is generated for
- **Jahr**: which calendar year to render
- **Sommerferien-Start**: Bavarian summer holiday start date (auto-fills for known years 2024–2030)
- **Geburtstage**: colleague birthdays to highlight

The tool automatically:

- Computes German/Bavarian public holidays (Easter-based + fixed dates) for the selected year
- Resolves the 6-year Jahresurlaub (annual leave) rotation across all 6 teams, splitting the summer-linked slots into two 4-week blocks (each with 3 weeks inside the actual school holidays)
- Substitutes "U" (Urlaub-Platzhalter) weeks in the rhythm with the covering team's actual shift pattern when a different team is on leave that week
- Prints in landscape with background colors preserved (`Drucken / als PDF speichern` button, or Ctrl+P / Cmd+P)

No data is stored or transmitted anywhere; all state lives only in the page while it's open.
