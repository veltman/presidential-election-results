# Presidential election results, 1976 - 2020

![Election results map](/voteshare.png)

Popular vote data for 1976-2016 comes from the [MIT Election Data and Science Lab](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/42MVDX) which is in turn sourced from the [Clerk of the U.S. House of Representatives](http://history.house.gov/Institution/Election-Statistics/Election-Statistics/).

Popular vote data for 2020 comes from the [New York Times](https://www.nytimes.com/interactive/2020/11/03/us/elections/results-president.html) as of December 7, 2020.

The columns are as follows:

- `year` - Election year
- `state` - State postal code
- `demVotes` - Democratic candidate votes
- `gopVotes` - Republican candidate votes
- `otherVotes` - Votes for third-party or no-party candidates (see below re: fusion parties)
- `totalVotes` - Total presidential votes in the state that year
- `demShareTotal` - Calculated as `demVotes / totalVotes`
- `gopShareTotal` - Calculated as `gopVotes / totalVotes`
- `demShareTwoParty` - Calculated as `demVotes / (demVotes + gopVotes)`
- `gopShareTwoParty` - Calculated as `gopVotes / (demVotes + gopVotes)`
- `differenceTotal` - The difference between the state's `demShareTotal` and the national `demShareTotal` for the same year
- `differenceTwoParty` - The difference between the state's `demShareTwoParty` and the national `demShareTwoParty` for the same year

The data has been cleaned as follows:

- Votes for a major party candidate under an alternate party have been counted under the major party when applicable (e.g. Democratic-Farmer-Labor votes in Minnesota and Working Families Party votes in New York are counted as Democratic votes if the Democratic candidate was listed)
- Known data entry errors in the MIT data have been corrected
