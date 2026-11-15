# Wayanad from orbit: before and after the Kalladi slide

An interactive page built for the **NASA Space Apps Challenge 2026 (Panaji)**, challenge *Dancing with the SARs*.
It uses NISAR L-band radar previews to compare Wayanad, Kerala, before and after the 7 July 2026 Kalladi landslide, and explains what the radar can and cannot show.

## What it does
- **Swipe comparison** of two NISAR radar previews: 27 Jun 2026 (10 days before the slide) and 9 Jul 2026 (2 days after).
- **Interferogram view** (4 Jul to 21 Aug 2026) with a plain-language reading of where phase holds, where it doesn't, and why.
- **A limits section** written for non-experts: what a radar preview is, why rain and display stretching can mimic change, and why a small slope failure won't show at this scale.

## Data (NISAR L-band, PROVISIONAL, CRID P05023, via ASF DAAC)
| Use | Granule |
|---|---|
| Before | `NISAR_L2_PR_GCOV_024_012_A_007_4005_DHDH_A_20260627T002415_20260627T002450_P05023_N_F_J_001` (browse image) |
| After | `NISAR_L2_PR_GCOV_025_012_A_008_4005_DHDH_A_20260709T002448_20260709T002523_P05023_N_F_J_001` (browse image) |
| Interferogram | `NISAR_L2_PR_GUNW_024_113_A_007_028_4000_SH_20260704T003235_20260704T003309_20260821T003232_20260821T003307_P05023_N_F_J_001` (browse image) |

Event context: Mongabay India, "Tunnel landslide raises fresh questions over mountain development" (July 2026).

## Method
1. Searched ASF Vertex (NISAR, 17 Jun to 31 Aug 2026) at Sultan Bathery, Wayanad.
2. Picked scenes on the same repeating track around the 7 July event.
3. Downloaded the small lat/lon browse images and footprint KMLs (not the multi-GB HDF5 files).
4. Cropped both previews to the same longitude/latitude window using the KML bounds (75.95 to 76.40 E, 11.40 to 11.80 N) and embedded them in one static HTML page.

## Limitations (important)
- Previews are display-stretched quick-looks, **not calibrated backscatter**, so brightness differences are qualitative only.
- The two images are different frames (007 and 008) of the same track. Wayanad is near the edge of both.
- The page does not show the landslide itself. Pin positions are approximate and the slide site is not marked.
- Data are provisional (calibrated, still being validated).

## Future work
- Measure calibrated GCOV backscatter at the slide site across all available dates (also 21 Jul, 14 Aug, 26 Aug on this track) to test whether a change persists (surface damage) or fades (soil moisture).
- Use a same-frame pair for 27 Jun and 9 Jul.
- Add infrastructure and slope layers for context, without claiming prediction.

## Run
Open `index.html` in a browser. No build step. Fonts load from Google Fonts; the page works without them.

## Credits
NISAR is a joint NASA-ISRO mission. Data distributed by the Alaska Satellite Facility DAAC. Built at NASA Space Apps Challenge 2026, Panaji.

## Licence
MIT (see `LICENSE`). NISAR data are subject to NASA/ASF data policies.
