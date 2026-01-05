<h1>Big Data Cup Submission Guidelines</h1>
<h2>Submission Rules & Guidelines:</h2>
<p>Maximum 6 pages, including figures (size limit 10GB on submission)</p>
<p>Format of submission:</p>
<ul>
  <li>Define your thesis </li>
  <li>Provide a summary of your methodology</li>
  <li>Give an overview of your findings</li>
  <li>Identify key action points from your analysis</li>
  <li>Code may be included as an appendix</li>
</ul>
<br>
<h2>Three Research Areas:</h2>
<p>This year's Big Data Cup offers three exciting research areas to explore! Tracking data must be used in any project.</p>
<p>Please identify in the title which area you will be focusing on:</p>
<b>1. Team Coordination</b>
<p>How do teams work together? Reveal valuable insights into team strategy and execution. Examples include:</p>
<ul>
  <li>Zone breakouts</li>
  <li>Forecheck</li>
  <li>Transition play</li>
  <li>Special teams configurations</li>
</ul>
<b>2. Skating Ability</b>
<p>How can skating be evaluated aside from speed? Redefine how skating ability is viewed to offer teams a deeper understanding of player performance. Examples include:</p>
<ul>
  <li>Skating agility and lateral movement</li>
  <li>Stamina over long shifts and throughout a game</li>
  <li>Movement profile when skating versus without the puck</li>
</ul>
<b>3. Player Movement</b>
<p>How do players' on-puck and off-puck movements influence team dynamics and game outcomes? Develop a better understanding of player actions and their ripple effects on the ice. Examples include:</p>
<ul>
  <li>Creating space for themselves and teammates while on the puck</li>
  <li>Defensive anticipation and positioning</li>
  <li>Offensive off-puck awareness and positioning</li>
</ul>
<p>Note: These examples are just starting points. Let your creativity shine!</p>
<br>
<h1>Dataset</h1>
<h2>Summary</h2>
<p>The dataset is comprised of Stathletes-tracked hockey event data, as well as player tracking data generated from broadcast video. The included events have been translated from Stathletes’ raw data to enhance accessibility and interpretability. The various event types include shots, plays, takeaways, puck recoveries, dump ins, dump outs, zone entries, faceoffs and penalties. Event definitions may slightly differ from other sources. For each event, expanded details are provided and the relevant skaters and teams involved are indicated when necessary.</p>

<h2>Downloading the Data</h2>
<p>https://github.com/bigdatacup/Big-Data-Cup-2025/releases/tag/Data</p>

<p><b>Examples:</b></p>
<p><b>Event Data:</b> 2024-10-13.Team.B.@.Team.A.-.Events.csv</p>
<p><b>Tracking Data:</b> 2024-10-13.Team.B.@.Team.A.-.Tracking.csv</p>
<p><b>Shifts Data:</b> 2024-10-13.Team.B.@.Team.A.-.Shifts.csv</p>
<p><b>Camera Orientation Index:</b> camera_orientations.csv</p>

<h2>Event Data</h2>
<ul>
  <li>Date (e.g. ‘2020-12-23’. Format = ‘yyyy-mm-dd’)</li>
  <li>Home Team (e.g. ‘Team A’)</li>
  <li>Away Team (e.g. ‘Team B’)</li>
  <li>Period (range from 1-3 for regulation, 4+ for overtime)</li>
  <li>Clock (e.g. ‘19:34’. Format = ‘mm:ss’)</li>
  <li>Home Team Skaters (range from 3-6 for home skaters currently on the ice)</li>
  <li>Away Team Skaters (range from 3-6 for away skaters currently on the ice)</li>
  <li>Home Team Goals (current goals scored by the home team at the time of the event)</li>
  <li>Away Team Goals (current goals scored by the away team at the time of the event)</li>
  <li>Team (ID of the team responsible for the event)</li>
  <li>Player (ID of the player responsible for the event)</li>
  <li>Event (type of event, e.g. ‘Play’, ‘Shot’, …)</li>
  <li>X Coordinate (x-coordinate of where an event occurred on the ice, between -100 and 100)</li>
  <li>Y Coordinate (y-coordinate of where an event occurred on the ice, between -42.5 and 42.5)</li>
    <ul>
      <li>Coordinates are from the perspective of the camera - index of team orientation in camera_orientations.csv</li>
    </ul>
  </li>
  </ul>
<img src = "rink_coords.png"></img>
 <ul>
 <li>Detail 1-4 (up to 4 supplementary details for each event, varies by event type)</li>
 <li>Player 2 (ID of a secondary player involved in an event, varies by event type)</li>
 <li>X Coordinate 2 (x-coordinate of a secondary event detail, varies by event)</li>
 <li>Y Coordinate 2 (y-coordinate of a secondary event detail, varies by event)</li>

</ul>

<br>

<br>

<h2>Tracking Data</h2>

Tracking Data Definitions: 
1. Image Id: A unique identifier for the game from which the player data was extracted 
2. Period: Period of the game  
3. Game Clock: Game Clock of the game 
4. Player or Puck: “Player” if the row refers to a player, “Puck” if the row refers to the puck 
5. Team: One of “Home”, “Away”, or “n/a” (if the puck) 
6. Player Id: The ID or jersey number of the tracked player. Every row for a specific Player Id will have the same jersey number. Player Jersey 
Number is blank if the tracked player’s jersey number couldn’t be identified. 
7. Rink Location X (Feet), Rink Location Y (Feet)
8. Rink Location Z (Feet): This column is always “1” for players and “0.02” for the puck, other than when a goal is scored. When a goal is scored, it’s the 
“Z” position of the puck (how high off the ice the puck is, in feet). 
9. Goal Score: If a goal is scored, this column will be “G” for 1 “Puck” row around when the puck enters the goal. For all other rows, it will be empty.  

<br>

<h2>Shifts Data</h2>

Shifts Data Definitions: 
1.  Date: Date of the game
2.  game_name: ID of the game
3.  team_name: ID of the team
4.  Player_Id: ID of the player
5.  shift_number: Shift number (in increasing order) for each player
6.  period: Period of the shift (range from 1-3 for regulation, 4+ for overtime)
7.  start_clock: Starting clock time of the shift (e.g. ‘19:34’. Format = ‘mm:ss’)
8.  end_clock: Ending clock time of the shift (e.g. ‘19:34’. Format = ‘mm:ss’)
9.  shift_length: Duration of the shift (e.g. ‘19:34’. Format = ‘mm:ss’)

<br>

<h2>Event Data Definitions</h2>
<h3>Shot</h3>
<p>Shot attempts that are unsuccessful (block, miss or save)</p>

<p>Players Involved</p>
<ul>
  <li>Player: Shooter </li>
</ul>

<p>Coordinates</p>
<ul>
  <li>X,Y Coordinate: Release location </li>
</ul>

<p>Event Details</p>
<ul>
  <li>Detail 1: Shot Type (Deflection, Fan, Slapshot, Snapshot, Wrap around, Wristshot)</li>
  <li>Detail 2: Shot destination (on net, missed or blocked)</li>
  <li>Detail 3: Traffic (true or false)</li>
  <li>Detail 4: One timer (true or false)</li>
</ul>
<br>

<h3>Goal</h3>
<p>Shot attempts that are successful (goal)</p>

<p>Players Involved</p>
<ul>
  <li>Player: Shooter </li>
</ul>

<p>Coordinates</p>
<ul>
  <li>X,Y Coordinate: Release location of the puck </li>
</ul>

<p>Event Details</p>
<ul>
  <li>Detail 1: Shot Type (Deflection, Fan, Slapshot, Snapshot, Wrap around, Wristshot)</li>
  <li>Detail 2: Shot destination (on net, missed or blocked)</li>
  <li>Detail 3: Traffic (true or false)</li>
  <li>Detail 4: One timer (true or false)</li>
</ul>
<br>



<h3>Play</h3>
<p>Pass attempts that are successful</p>

<p>Event Types</p>
<ul>
  <li>Direct (e.g. a tape-to-tape pass)</li>
  <li>Indirect (e.g. a pass that is rimmed along the boards) </li>
</ul>

<p>Players Involved</p>
<ul>
  <li>Player: Passer </li>
  <li>Player 2: Intended pass target</li>
</ul>

<p>Coordinates</p>
<ul>
  <li>X,Y Coordinate: Pass release location</li>
  <li>X,Y Coordinate: Pass target location</li>
</ul>

<p>Event details</p>
<p>Detail 1: Pass Type</p>
<ul>
  <li>Direct (eg. a tape-to-tape pass)</li>
  <li>Indirect (eg. a pass that is rimmed around the boards)</li>
</ul>
<br>

<h3>Incomplete Play</h3>
<p>Pass attempts that are unsuccessful</p>

<p>Event Types</p>
<ul>
  <li>Direct (e.g. a tape-to-tape pass)</li>
  <li>Indirect (e.g. a pass that is rimmed along the boards) </li>
</ul>

<p>Players Involved</p>
<ul>
  <li>Player: Passer </li>
  <li>Player 2: Intended pass target</li>
</ul>

<p>Coordinates</p>
<ul>
  <li>X,Y Coordinate: Pass release location</li>
  <li>X,Y Coordinate: Pass target location</li>
</ul>

<p>Event details</p>
<p>Detail 1: Pass Type</p>
<ul>
  <li>Direct (eg. a tape-to-tape pass)</li>
  <li>Indirect (eg. a pass that is rimmed around the boards)</li>
</ul>
<br>


<h3>Takeaway</h3>
<p>Steals, pass interceptions and won battles that lead to a change in possession</p>

<p>Players Involved</p>
<ul>
  <li>Player: Skater credited with the takeaway </li>
</ul>

<p>Coordinates</p>
<ul>
  <li>X,Y Coordinate: Location where the skater gained possession when taking the puck away</li>
</ul>
<br>

<h3>Puck Recovery</h3>
<p>Possession gains initiated by retrieving a loose puck that was created by a missed/blocked/saved shot, an advance (e.g. dump-out/dump-in), a faceoff or a broken play</p>

<p>Players Involved</p>
<ul>
  <li>Player: Skater who recovered the puck</li>
</ul>

<p>Coordinates</p>
<ul>
  <li>X,Y Coordinate: Location where skater gained possession</li>
</ul>
<br>
<h3>Dump In/Out</h3>
<p>Actions in which a skater intentionally concedes possession by advancing the puck up ice</p>

<p>Players Involved</p>
<ul>
  <li>Player: Skater who dumped/advanced the puck</li>
</ul>

<p>Coordinates</p>
<ul>
  <li>X,Y Coordinate: Location where skater released the puck</li>
</ul>
<p>Event details</p>
<ul>
  <li>Detail 1: Possession Outcome (Retained, Lost)</li>
</ul>

<br>
<h3>Zone Entry</h3>
<p>Attempts to move the puck into the offensive zone from the neutral zone</p>

<p>Players Involved</p>
<ul>
  <li>Player: Entry skater</li>
  <li>Player 2: Targeted defender</li>
</ul>

<p>Coordinates</p>
<ul>
  <li>X,Y Coordinate: Point of release for dumps/advances, point where puck crossed the blueline for passes and carries</li>
</ul>

<p>Event details</p>
<ul>
  <li>Detail 1: Entry Type (Carried, Dumped, Played)</li>
</ul>

<br>
<h3>Faceoff Win</h3>
<p>Faceoffs</p>

<p>Players Involved</p>
<ul>
  <li>Player:  Skater who won the draw</li>
  <li>Player 2: Skater who lost the draw</li>
</ul>

<p>Coordinates</p>
<ul>
  <li> X,Y Coordinate: Location of faceoff dot</li>
</ul>

<br>
<h3>Penalty Taken</h3>
<p>Infractions</p>


<p>Players Involved</p>
<ul>
  <li>Player: Skater who took the penalty</li>
  <li>Player 2: Skater who drew the penalty</li>
</ul>

<p>Coordinates</p>
<ul>
  <li>X,Y Coordinate: Location of infraction</li>
</ul>

<p>Event Details</p>
<ul>
  <li>Detail 1: Infraction Type (e.g. Slashing, Tripping, Roughing, Hooking, ...)</li>
</ul>

