# Into the (HIPAA) Breach

If I asked, you’d probably say credit card breaches are the worst, right? Since your credit could be ruined forever?

HIPAA breaches are serious too, though the consequences may not be as readily apparent. Like with credit card breaches, one possible consequence is identity theft, but even more concerning is if a breach involves malware designed to harm a system – the consequences could be disruptive and devastating, especially for more vulnerable populations.

Slide deck here: https://docs.google.com/presentation/d/1LQ14x4bs55n4JD-ytRXBLPtoCH17T4NV3vm8CfmM0hw/
Dashboard here: https://public.tableau.com/app/profile/ctrlvng/viz/IntotheHIPAABreach_16705938852440/IntotheHIPAABreach

### About the Data & Libraries

The data comes from the Office of Civil Rights, which publicly updates a list of breaches affecting 500 or more individuals here: https://ocrportal.hhs.gov/ocr/breach/breach_report.jsf 

I also used 2021 population estimate data from the U.S. Census to quantify state impact: https://www.census.gov/data/tables/time-series/demo/popest/2020s-national-total.html

There are two types of investigations of HIPAA breaches: current/open and archive/closed. The latter contains an additional column of summaries of how the breach unfolded. The last segment of this project (stored in this repository) is the analysis I conducted to categorize hacking-related keywords in the summaries, in order to understand more recent trends in types of hacking incidents.

I used the Pandas and PandaSQL libraries libraries for data exploration.

### Categorization of Hacking-Related Keywords Method

I first used Pandas to randomly sample 50 summaries and manually categorized them, in order to create a list of keywords to categorize by. Then, I used PandaSQL to categorize the summaries by keyword.

### Limitations

Consider the keyword “spyware,” which allows someone to monitor your computer activities. “Spyware” appears only twice in all of the data, and both in the context of installing anti-spyware, which is why number of mentions does not directly translate to number of hacking incidents.

Moreover, the summaries do not provide a lot of technical detail, likely because this is public data, and outlining specific vulnerabilities would put the listed entities at greater risk. The vague descriptions often use interrelated keywords and don’t always distinguish between mode of entry, like phishing, and the actual attack, such as ransomware.
