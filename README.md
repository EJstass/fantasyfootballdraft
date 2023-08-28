<h1>
            Fantasy Football Draft
        </h1>
          <div class="text">
          <h2>
            Foreword
        </h2>
          <p>
            I have played Fantasy Football since my Freshman year at the University of Connecticut.
            I love watching the NFL and making projections about how many points my team will score.
            Over time, I joined more leagues and spent more times making projections.
            At this point I'm in 4 leagues and don't have enough time to plan strategies and make projections for all of them.
            My biggest emphasis was always on drafting players because it's the most significant moment that will make or break the season.
            Unfortunately, ESPN always had low expectations for the teams I drafted.
            Interestingly enough, I'm usually able to restock my teams via Free Agency over the course of the season to the point where it's fairly uncommon for me to miss the playoffs.
            However, I wondered what I could do to improve my drafts.
            The following project aims to maximize the returns of every Snake draft for any size league for any scoring format for any year.
            If you're unfamiliar with Fantasy Football, check it out <a target="_blank" rel="noopener noreferrer" href="https://www.espn.com/fantasy/football/story/_/page/nfldk2k14intro/first-timer-guide">here.</a>
          </p>
        <h2>
            Abstract
        </h2>
          <p>
            Fantasy Football Drafts are the primary opportunity to put your team in a position to win your league.
            At the beginning of the season you start with an empty team and it's up to you to decide which player to take at each round of the draft.
            Everyone has their own strategy that may or may not work out.
            Most of the decision-making is based on the position of the player and the projected points for the season.
            ESPN provides projections for total Fantasy Points and in general the number of players per position is obvious.
            However, given the players available, how do you decide the most valuable combination of position and projected points?
            The following project uses Monte Carlo Simulations to determine the best pick at each round of the draft and integrates those predictions with ESPN to make drafting simple.
          </p>
        <h2>
            Introduction
        </h2>
          <h3>
            Game Rules
          </h3>
          <p>
            I am far from the first person to describe Fantasy Football.
            A comprehensive overview of the rules can be found  <a target="_blank" rel="noopener noreferrer" href="https://www.espn.com/fantasy/football/story/_/page/nfldk2k14intro/first-timer-guide">here.</a>
            My leagues are generally 12-person, Snake Draft, .75 PPR and 16 player teams (1 QB, 2RB, 2WR, 1TE, 1Flex, 1D/ST, 1K, 7Bench).
            </p>
          <h3>
          <h3>
            Data Collection
          </h3>
            <p>
              Prior to every draft, ESPN allows you to view/edit the predraft rankings.
              The rankings are a goldmine for drafting data because it easily outlines every player's team, position, and projected fantasy points.
              ESPN projects each player's fantasy points for you and constantly updates them based on what's happening in the NFL.
              To collect this data, you simply need to scrape it off the website.
            </p>
        <h2>
            Preliminary Works
        </h2>
        <h3>
          Monte Carlo Simulations
        </h3>
            <p>
              The Monte Carlo Method is a technique that use simulations of a scenario to determine the possible outcomes.
              For example in a draft setting, Monte Carlo Simulations can find all the possible picks by each team.
              Based on all the possible picks, it can determine the best pick based on the current conditions of the draft.
              Obviously this can be very useful in a Fantasy Football draft setting.
              Fortunately, I was able to find this <a target="_blank" rel="noopener noreferrer" href="https://towardsdatascience.com/using-monte-carlo-tree-search-for-your-fantasy-football-draft-6509b78a1c20">post</a> by <a target="_blank" rel="noopener noreferrer" href="https://medium.com/@ykeuter?source=post_page-----6509b78a1c20--------------------------------">Yvo Keuter</a>.
              Yvo built a pipeline that will draft via Monte Carlo for every team in the league.
            </p>
        <h2>
            Experiments
        </h2>
        <h3>
          ESPN Integration
        </h3>
        <p>
          Yvo wrote code that was in excellent condition for me apply to any ESPN draft.
          I only had to adjust it pull data from the ESPN pre-draft rankings, adjust the to only use Monte Carlo Simulations for one team, and monitor the picks from other teams.
          I managed to connect to EXPN using Selenium and BeautifulSoup in Python. 
          This solution was ideal because I didn't have to constantly connect to ESPN with an API and Selenium would open a browser for me to interact with in real-time.
          The final code has been posted to my Github <a target="_blank" rel="noopener noreferrer" href="https://github.com/EJstass/fantasyfootballdraft">here</a>.
        </p>
        <h3>
          Outcome
        </h3>
        <p>
          I connected to several ESPN Mock Drafts to test out the effectiveness of the draft choices.
          Check out the Youtube video below that demos one of those Mock drafts.
          As you can see at the end of the video, my team had the highest projected fantasy points.
          https://www.youtube.com/embed/q53NkWhQLT8?si=58otnRtFJUiPTlzD
        </p>
        <h2>
            Conclusion
        </h2>
          <p>
            As shown in the video, the implementation is very smooth and concise.
            The recommendations from the algorithm are determined automatically and they can help you pick a team that has above average projected Fantasy points.
            The remaining question is whether high projected fantasy point totals actually help you win.
          </p>
          <p>
            Let's see how this season goes!
          </p>
        <h2>
            Citations
        </h2>
          <p>
            Yvo Keuter: <a target="_blank" rel="noopener noreferrer" href="https://towardsdatascience.com/using-monte-carlo-tree-search-for-your-fantasy-football-draft-6509b78a1c20">Post</a> 
          </p>
        <h2>
            My Links
        </h2>
          <p>
            GitHub: <a target="_blank" rel="noopener noreferrer" href="https://github.com/EJstass/fantasyfootballdraft">fantasyfootballdraft</a>
          </p>
