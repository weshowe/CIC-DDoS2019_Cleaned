# CIC-DDoS2019_Cleaned
After cleaning the CIC-DDoS2019 dataset from UNB, it was noticed that it had a large number of duplicate rows. The cleaned dataset with no duplicates is presented here in ZIP files for convenience.

Cleaning Procedure:

1. Each CSV file from CIC-DDoS2019 is loaded.
2. The columns 'Flow ID', ' Source IP', ' Source Port', ' Destination IP',' Destination Port', and ' Timestamp' are dropped.
3. All rows containing null or infinity values (np.inf, -np.inf) are dropped.
4. All rows with non-numeric feature values are dropped.
5. Duplicates are removed using df.drop_duplicates() from Pandas.
6. The resulting CSV is saved with "_cleaned" appended to the file name.

Total Day 1 size before cleaning and duplicate removal: 8.14 GB

Total Day 1 size after cleaning and duplicate removal: 910 MB

Total Day 2 size before cleaning and duplicate removal: 20.7 GB

Total Day 2 size after cleaning and duplicate removal: 3.22 GB

Original Dataset available at: https://www.unb.ca/cic/datasets/ddos-2019.html

Reference:
Iman Sharafaldin, Arash Habibi Lashkari, Saqib Hakak, and Ali A. Ghorbani, "Developing Realistic Distributed Denial of Service (DDoS) Attack Dataset and Taxonomy", IEEE 53rd International Carnahan Conference on Security Technology, Chennai, India, 2019.
