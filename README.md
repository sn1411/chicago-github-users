# GitHub Users Analysis
- This project scrapes GitHub users in Chicago with over 100 followers and their repositories using the GitHub API.
- An interesting insight is that most popular repositories are dominated by a few programming languages like JavaScript, Python and Ruby.
- Developers may consider focusing on these languages for wider reach and community support in Chicago's GitHub ecosystem.

# More about ...
## Data Collection
The data was collected using the **GitHub API**, specifically targeting users located in **Chicago** with a minimum of **100 followers**. The following steps were taken:
1. **API Access**: Utilized the GitHub API to query user data based on geographical location and follower count.
2. **Data Scraping**: Extracted user profiles, including their repositories, ensuring that all relevant information was captured for further analysis.

## Data Description
The data used for this analysis includes information about GitHub users, such as:
1. **users.csv** has following information about each user in Chicago with over 100 followers, with fields:
    login: Their Github user ID
    name: Their full name
    company: The company they work at.
    location: The city they are in
    email: Their email address
    hireable: Whether they are open to being hired
    bio: A short bio about them
    public_repos: The number of public repositories they have
    followers: The number of followers they have
    following: The number of people they are following
    created_at: When they joined Github

2. **repositories.csv** has these users' public repositories. For each user in users.csv, up to the 500 most recently pushed repositories were fetched, with fields:
    login: The Github user ID (login) of the owner, which, BTW, is not directly in the API response.)
    full_name: Full name of the repository
    created_at: When the repository was created
    stargazers_count: Number of stars the repository has
    watchers_count: Number of watchers the repository has
    language: The programming language the repository is written in
    has_projects: Whether the repository has projects enabled
    has_wiki: Whether the repository has a wiki
    license_name: Name of the license the repository is under (This is under license.key)

## Key Analyses
1. **Most Common Surname**: 
   - Analyzed user names to determine the most frequently occurring surname. In case of a tie, all surnames were listed in alphabetical order.

2. **Correlation Analysis**: 
   - Examined the correlation between various metrics such as:
     - Followers vs. Public Repositories
     - Projects enabled vs. Wiki enabled

3. **Regression Analysis**:
   - Estimated the relationship between the number of public repositories and followers to determine how additional repositories impact follower count.

4. **Comparative Analysis**:
   - Compared hireable users to non-hireable users regarding their average number of followers, public repositories, and whether they share their email addresses.

## Conclusions
The analysis provides insights into how GitHub users in Chicago engage with the platform and how certain factors (like having more repositories or a complete profile) may influence their visibility and connections.

## Acknowledgments
Thanks to the contributors and datasets used in this analysis.