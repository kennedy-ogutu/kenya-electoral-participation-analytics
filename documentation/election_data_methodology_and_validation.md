# Kenya Electoral Participation Analytics
## Data Methodology and Validation Summary

### 1. Project scope

This dataset contains county-level presidential election
information for Kenya's 47 counties across four election events:

- 2013 General Election
- August 2017 General Election
- October 2017 Fresh Presidential Election
- 2022 General Election

The October 2017 election is treated as a distinct electoral
event rather than a separate general election.

### 2. Data sources

The project uses election information extracted from
ELOG reports and official IEBC election documents.

ELOG data provides the initial county-level election records.

IEBC documents provide official county-level figures used
for reconciliation where available.

The availability and completeness of official county-level
figures differ across election events.

### 3. Analytical measures

**Registered voters**

The selected registration denominator for each county
and election event.

**Valid votes**

The selected count of valid presidential votes.

**Ballots cast**

The selected count of ballots cast, including rejected
ballots where those components are available.

**Calculated turnout (%)**

Calculated as:

    (Analytical ballots cast / Analytical registered voters) * 100

**Valid-vote participation (%)**

Calculated as:

    (Analytical valid votes / Analytical registered voters) * 100

**Source-reported turnout (%)**

The turnout percentage reported in the ELOG source.

This is retained separately from calculated turnout.

### 4. Election-specific reconciliation decisions

#### 2013 General Election

- Registration uses the IEBC total registered-voter count,
  including biometric and non-biometric registration.
- Analytical valid votes are retained from ELOG.
- Ballots cast use the IEBC number-voted field.
- All 47 county records are classified as partially reconciled.
- Differences in turnout definitions and denominators
  require care when comparing source-reported percentages.

#### August 2017 General Election

- Registration uses IEBC county figures.
- Valid votes and rejected ballots use IEBC county figures
  where the source reconciliation is acceptable.
- Ballots cast are calculated from valid votes plus
  rejected ballots for reconciled records.
- 45 counties have matched vote-count records.
- Kisumu is flagged for an internal inconsistency in
  the printed IEBC source.
- Turkana is flagged for an unresolved difference
  between ELOG and IEBC valid-vote figures.
- Analytical valid votes, ballots cast and calculated
  turnout remain missing for Kisumu and Turkana.

Two additional turnout discrepancies are documented:

- Kirinyaga: calculated 87.15%; ELOG reported 86.11%.
- Kericho: calculated 78.64%; ELOG reported 80.78%.

These are turnout-specific discrepancies and do not
replace the vote-count reconciliation statuses.

#### October 2017 Fresh Presidential Election

- Registration and valid-vote counts match the available
  official county figures for all 47 counties.
- Ballots cast are calculated from IEBC valid votes
  and rejected ballots.
- The election is analysed as a distinct event.

#### 2022 General Election

- County registration and valid-vote figures are
  retained from ELOG.
- Independent reconciliation against official
  county-level results has not been completed.
- Analytical ballots cast and calculated turnout
  remain unavailable for all 47 counties.
- Valid-vote participation is available but relies
  on the provisional county figures.
- ELOG-reported turnout is retained as a separate field.

### 5. Presidential candidate results

Winner, winner-vote, runner-up and margin fields
are derived from ELOG.

Basic numerical integrity checks were completed:

- Winner votes do not exceed available analytical valid votes.
- Winner-vote counts are nonnegative.
- Margins are nonnegative.
- Margins do not exceed winner votes.

These checks do not constitute independent candidate-level
reconciliation against official IEBC results.

### 6. Validation outcomes

- Total election-county records: 188
- Counties per election event: 47
- Official county records successfully joined: 141
- Duplicate election-county records: 0
- Final structural and participation checks passed: 11 of 11
- Presidential-result integrity checks flagged: 0 records
- August 2017 unresolved valid-vote records: 2
- August 2017 turnout discrepancies above 1 pp: 2
- Missing analytical ballots-cast values: 49

Passing these checks establishes consistency with the
documented analytical rules. It does not independently
verify every underlying source figure.

### 7. Dataset outputs

**Working dataset**

    data/Interim/election_county_integrated_working.csv

Contains 188 records and 34 fields, including supporting
source and reconciliation information.

**Processed analytical dataset**

    data/Processed/kenya_county_election_analytics.csv

Contains 188 records and 20 fields selected for analysis.

### 8. Analytical limitations

- Calculated turnout and valid-vote participation are
  different measures and should not be interchanged.
- August and October 2017 must remain distinct events.
- The two unresolved August 2017 county records should
  not be silently included in aggregate calculations
  requiring missing analytical values.
- The 2022 county data remains independently unverified.
- Source-reported 2022 turnout should not be presented
  as independently calculated turnout.
- Comparisons across election years must acknowledge
  differences in source coverage and methodology.

### 9. Reproducibility

The project preserves original raw source files,
intermediate extracted datasets, reconciliation registers,
turnout discrepancy documentation and analytical outputs.

Source discrepancies are documented rather than silently
corrected.
