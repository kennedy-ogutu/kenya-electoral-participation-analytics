# Kenya Electoral Participation Analytics
## County-Level Presidential Election Analysis, 2013–2022

### Executive Summary

This project examines presidential electoral participation across
Kenya's 47 counties, focusing on the relationship between voter
registration growth and valid-vote participation.

Between 2013 and 2022, valid-vote participation declined in all
47 counties.

Across the complete 47-county endpoint sample:

- Registered voters increased by
  **53.69%**.
- Valid presidential votes increased by
  **16.27%**.
- Weighted valid-vote participation declined from
  **84.93%**
  to **64.26%**.
- The weighted participation decline was
  **20.68
  percentage points**.
- The unweighted mean county decline was
  **19.25
  percentage points**.

These findings describe changes in electoral participation.
They do not establish the causes of those changes.

### 1. Research Objectives

The analysis addresses four questions:

1. How did valid-vote participation change between 2013 and 2022?
2. How did registration growth compare with valid-vote growth?
3. How did participation trends vary across counties?
4. How did turnout change between the August and October 2017
   presidential elections?

### 2. Data and Methodology

The analytical dataset contains 188 county-election records:
47 counties across four presidential electoral events.

The events are:

- 2013 general election
- August 2017 general election
- October 2017 fresh presidential election
- 2022 general election

The October 2017 election is treated as a separate electoral
event rather than an ordinary general election.

#### Key measure

Valid-vote participation is calculated as:

**Valid-vote participation (%) =
(valid presidential votes / registered voters) × 100**

This measure is distinct from turnout based on ballots cast.

#### Analytical samples

The direct 2013–2022 endpoint analysis uses all **47 counties**.

Comparisons requiring August 2017 valid-vote participation
use **45 counties**, excluding Kisumu and Turkana because of
unresolved discrepancies between the ELOG and IEBC August 2017
valid-vote figures.

The same 45-county restriction is used for the August–October
2017 turnout comparison.

### 3. Electoral Participation, 2013–2022

Weighted valid-vote participation declined from
**84.93%** in 2013 to
**64.26%** in 2022.

All 47 counties recorded a decline.

The mean county decline was
**19.25 percentage points**.

The previously prepared three-election visualisation uses the
45-county comparable sample and should be interpreted on that basis.

![General election participation: 45-county sample](
figures/01_general_election_valid_vote_participation.png
)

### 4. County-Level Differences

Participation declined in every county between 2013 and 2022,
although the magnitude of decline varied geographically.

Kisumu's valid-vote participation fell from 89.79% to 70.95%,
a decline of 18.84 percentage points.

Turkana's participation fell from 75.04% to 60.17%,
a decline of 14.87 percentage points.

The existing county-ranking figure uses the 45-county
three-election sample.

![County participation declines: 45-county sample](
figures/02_county_participation_declines_2013_2022.png
)

### 5. Registration Growth Versus Valid-Vote Growth

Across all 47 counties between 2013 and 2022:

- Registration increased by
  **53.69%**.
- Valid votes increased by
  **16.27%**.

Registration therefore expanded substantially faster than
the number of valid presidential votes.

This divergence explains the decline in the ratio of valid
votes to registered voters.

The existing growth visualisation uses the 45-county sample,
for which registration increased by
**53.36%**
and valid votes by
**15.82%**.

![Registration and valid-vote growth: 45-county sample](
figures/03_registration_vs_valid_vote_growth_2013_2022.png
)

### 6. August–October 2017 Turnout

The August 2017 general election and October 2017 fresh
presidential election are analysed as distinct events.

Among the 45 counties with reconciled comparable turnout
figures, every county recorded a decline between the two events.

The unweighted mean county turnout decline was
approximately **39.09 percentage points**.

The comparison is descriptive and does not, by itself,
explain the political or behavioural causes of the change.

![August–October 2017 county turnout comparison](
figures/04_august_october_2017_county_turnout_comparison.png
)

![August–October 2017 turnout decline distribution](
figures/05_august_october_2017_turnout_decline_distribution.png
)

### 7. Source Reconciliation and Assurance

The analysis uses ELOG-derived county figures, with additional
reconciliation against published IEBC materials and a
2022 secondary transcription.

**2013:** County-level registration figures were reconciled
against an IEBC source. A difference of 2,637 voters remains
between the extracted county registration sum and the cited
national registration benchmark.

**August 2017:** Registration figures matched across all
47 counties. Kisumu and Turkana had unresolved valid-vote
differences and were excluded from analyses requiring those
August 2017 values.

**October 2017:** County registration and valid-vote figures
matched the IEBC comparison source across all 47 counties.

**2022:** ELOG registration and reported valid-vote totals
matched the Takwimu transcription for all 47 counties.

Two internal candidate-sum exceptions remain in the
Takwimu transcription:

- Kilifi: candidate-vote sum 10 below reported valid votes.
- West Pokot: candidate-vote sum 100 below reported valid votes.

The original signed IEBC Form 34C has not been independently
authenticated for this exercise. The 2022 assurance level is
therefore **secondary-source reconciled**, not officially verified.

### 8. Sensitivity Analysis

The original 45-county three-election sample and the complete
47-county endpoint sample produce closely aligned results.

| Measure | 45 counties | 47 counties |
|---|---:|---:|
| Counties with declining participation | 45 | 47 |
| Mean county decline (pp) | 19.36 | 19.25 |
| Weighted decline (pp) | 20.78 | 20.68 |
| Registration growth (%) | 53.36 | 53.69 |
| Valid-vote growth (%) | 15.82 | 16.27 |

Including Kisumu and Turkana does not change the direction
of the central 2013–2022 finding.

### 9. Limitations

- The analysis is descriptive, not causal.
- Valid-vote participation must not be described as
  ballots-cast turnout.
- Some historical source discrepancies remain unresolved.
- The 2022 reconciliation uses a secondary transcription
  attributed to Form 34C rather than a directly authenticated
  copy of the original signed declaration.
- The 45-county and 47-county samples must not be conflated.
- County-level aggregation cannot establish individual
  voter motivations or behaviour.

### 10. Conclusion

Between 2013 and 2022, Kenya's registered electorate grew
considerably faster than the number of valid presidential votes.

Valid-vote participation declined in all 47 counties,
indicating that the pattern was geographically widespread
rather than limited to a small group of counties.

The project demonstrates how transparent source
reconciliation, sample selection, reproducible calculations
and visual analysis can support a more reliable understanding
of electoral participation.

### Reproducibility

The project contains six sequential Jupyter notebooks,
intermediate and processed datasets, reconciliation registers,
validation summaries and five publication-ready figures.

All original source files are retained separately from
processed analytical outputs.
