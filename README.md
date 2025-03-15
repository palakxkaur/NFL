# Team Name

71552 Group 4

# Team Members

Ashleigh Myers @ashleigh-myers
Daniel Ding @dd68158
Shraeyas Muthaiah @shraeyasam
Palak Kaur @palakxkaur 
Zoe Jordan @Zoejordan012


# Problem Description
Our NFL database was created as a representation of a database that would aid the leaders or administrators of the football league to make critical, impactful decisions about the league, and facilitate management. It comprises key categories of information including the stadium, game, team, players, head coach, and tickets. The NFL is one of the biggest players in a huge sports and entertainment industry, and there is a huge amount of data that needs to be organized, managed, and utilized. Sports leagues constantly undergo change in response to unfair treatment of players, exploitation of rules by players and teams, or changing tastes of consumers. With our database, the league managers and its committees can interpret information to make informed decisions for the integrity, sustainability, and profitability of the league, along with handling the tasks they are responsible for, including creating or changing rules, approving ownership changes, training game officials, integrating technology, ensuring competitive balance, and maintaining legitimacy and entertainment of the game.

# Data Model
This data model outlines the structure of our sports management system, capturing key entities and their relationships. Starting with the stadium, it stores details about the location, capacity, and year built. It’s also linked to the game entity, showing where each game is played.
The game table captures game specifics like date, score, and the winning team. It connects the stadium and the team entities, linking the venue and participating teams. Additionally, it relates to tickets, tracking sales for each event.
The team entity holds information on the team’s founding date, wins, and losses. It’s connected to players and the head coach, creating a clear hierarchy of team composition.
Players are associated with a specific team and include personal details like name and position.
The head coach entity tracks the coach’s name and tenure, directly linking to the team they lead.
Tickets provide details on seat numbers, prices, and types. They link back to the game, stadium, and teams involved, to have a comprehensive event tracking. 
# NFL<img width="632" alt="Screenshot 2025-03-14 at 10 22 19 PM" src="https://github.com/user-attachments/assets/0d01c9e5-a2ca-4c0e-a000-d80ee344f69a" />
# Data Dictionary


<img width="703" alt="Screenshot 2025-03-14 at 10 22 56 PM" src="https://github.com/user-attachments/assets/e660d554-f5ad-4651-afab-ab9b7b920bdd" />

<img width="741" alt="Screenshot 2025-03-14 at 10 24 10 PM" src="https://github.com/user-attachments/assets/4dbefc97-5590-43b5-aa74-40aaa4e79e32" />


# Queries
** explain each query and why they are important to managers, basically what was on the slides but in paragraph form, include a screenshot of the query and output from SQL

Get Coaches of Teams with Above Average Wins
<img width="732" alt="Screenshot 2025-03-14 at 10 24 52 PM" src="https://github.com/user-attachments/assets/b315b620-73a0-44ff-85d8-4f1ccf828137" />
This query selects the coach's name, team name, and number of wins by joining the team and head coach table and selecting the coaches with wins above the average of other teams. This query is important to managers in the NFL for a variety of reasons. This can help evaluate the coaches' performance compared to their peers. This can be helpful when considering awards, brand deals/commercials, and hiring and recruitment. These high-performing coaches may be people that are more deserving of awards and certain brand deals. When other teams want to recruit coaches this may be a good way to find ones that are already performing well at their current teams. 

Games with scores above teams average
<img width="775" alt="Screenshot 2025-03-14 at 10 25 43 PM" src="https://github.com/user-attachments/assets/8f8b3339-eb65-4586-9583-3daf8801e327" />
It selects the game_id, date, score, and winning_team from the game table. It only includes games where the score is greater than the team's average score.This subquery shows the average score for all games played by that team. The outer query then compares each game's score to the average calculated by the subquery. If the game's score is above the average, it gets included in the result set. This query highlights games where a team performed better than usual, based on their scoring average. It helps in identifying high-performance games and understanding when a team exceeded expectations. Managers can use this information for analyzing games where the team scored above their average helps evaluate performance trends, highlighting peaks and consistency over time. By examining these high-scoring games, managers can identify key success factors, such as effective play strategies or player combinations that contribute to superior results. This insight supports game planning and strategic adjustments, allowing teams to refine their approach for upcoming matches. Additionally, it enables a deeper analysis of player impact, helping managers assess the influence of specific players or play-calling decisions on scoring performance. Furthermore, comparing these high-scoring games against opponents’ performance trends offers valuable competitive benchmarking, revealing strengths to leverage and weaknesses to address.

Query 3 lists the highest revenue games, along with the date, winning team, and the city of the game, by ticket sales/revenue in descending order.
<img width="738" alt="Screenshot 2025-03-14 at 10 26 20 PM" src="https://github.com/user-attachments/assets/f67e5d37-0a38-467e-a0c5-d8d6841a239a" />
To a league manager, the above query results would be useful to evaluate sources of funding, find out what teams or locations encourage engagement, and determine which teams and matchups to advertise and sell broadcast rights to for national TV. Furthermore, the query can be used to help create the season schedule, set appropriate ticket prices, and tailor local marketing strategies in ways that maximize viewership.

Teams with stadium capacity above average
<img width="720" alt="Screenshot 2025-03-14 at 10 26 59 PM" src="https://github.com/user-attachments/assets/13b62917-4762-41e7-95cd-63ad0daab82a" />
The information from this query displays the team name, stadium name, and the stadium capacity of the stadium where the capacity of each stadium is greater than the average capacity of all the stadiums. This would be important to managers because they would be able to tell how to set the price of tickets depending on the amount of customers. Thinking even further, they can determine where to host the Super Bowl as the popularity of the stadium and/or game can also be determined from this information.

Players in teams with most wins
<img width="746" alt="Screenshot 2025-03-14 at 10 27 47 PM" src="https://github.com/user-attachments/assets/7de1d328-bf8d-4b96-8476-35c3d2b948bd" />
This query retrieves the first name, last name, position, and team name of players who belong to the team with the most wins. This would be important for the NFL because it helps identify key players on the most successful team. Analysts and managers could use this information to study what makes the team successful, whether it be player performance, coaching strategies, or team composition. It could also be useful for marketing and promotional efforts because the league might want to highlight these top-performing players in advertising, media coverage, or award considerations.

Find players in a specific team
<img width="726" alt="Screenshot 2025-03-14 at 10 28 24 PM" src="https://github.com/user-attachments/assets/662d549a-6e20-4d59-a07c-a5c905ab9a1a" />
This query selects the name and position of players from a specific team. You can adjust which team you are looking at by changing the team id number. Having the ability to quickly generate a list of players in a specific team can be very valuable to NFL managers. This is critical to roster management, helping managers decide which adjustments need to be made to rosters. This is also important for recruitment, teams can see which positions they need more players for as well as other teams can use this data for negotiations for potential trades. 

Get head coach of each team
<img width="738" alt="Screenshot 2025-03-14 at 10 29 08 PM" src="https://github.com/user-attachments/assets/9b997cdc-12ff-40da-a917-b477a8e18c25" />
This query finds the head coach for each team by connecting the team and head_coach tables using the coach_id. It shows the team name along with the coach’s first and last name. This is useful for managers because it helps them quickly see who is leading each team. Knowing the head coach for every team makes it easier to track performance, make coaching decisions, and improve communication within the organization. It also helps in planning training, hiring new coaches, or making changes if needed.

Query 8 lists all players’ names and their teams.
<img width="702" alt="Screenshot 2025-03-14 at 10 29 46 PM" src="https://github.com/user-attachments/assets/02bf0461-1f2c-4529-a0d7-9437319b6d6c" />
This simple query provides all players’ first and last names along with the team they play for. A league manager can use these findings to look up any player of interest and see which team they play for. Subsequently, the manager can create roster lists, conduct physical investigations or inspections at the desired team practice facility, manage trades and signings, track payroll, and connect performance metrics with a specific player and team.


List all games with stadium information
<img width="719" alt="Screenshot 2025-03-14 at 10 30 22 PM" src="https://github.com/user-attachments/assets/ae50d750-af6b-4abe-9bdb-fd78cf9a777c" />
The information in this query displays the game ID, the date of the game, the score of the game, the stadium name, and the city the stadium is in. A manager can look at this data and determine where the higher scoring games took place. WIth this information, ticket prices can be adjusted and it can also show how much revenue/loss to expect in the future games based on the previous games.


Coaches with above-average tenure
<img width="714" alt="Screenshot 2025-03-14 at 10 31 39 PM" src="https://github.com/user-attachments/assets/ce9dbace-0eff-4e5c-a980-5cf68d001a0f" />
This query displays the name and tenure of head coaches who have a tenure that is longer than the average of all head coaches. For the league manager this information can be very useful in judging coach performance, conducting investigation into questionable team/coach relationships, deciding who to award (ex. Coach of the Year), and determining which coaches should be marketed more in a way that boosts revenue and engagement with football fans.


# Database Information
Name of the database: ha_group4_crn71552
<img width="669" alt="Screenshot 2025-03-14 at 10 37 35 PM" src="https://github.com/user-attachments/assets/b74128e1-eb48-4294-9514-3b4c55a993e1" />























