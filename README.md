# lol-replay-analysis
Replay assist tool designed to track choices made during a game and analyze what decisions could've been made differently


Brainstorming:
% Of winning a fight given current states
Don’t make the advice overcomplicated (Don’t say to memorize everything)

Future Ideas:
CDs: Kindred Bountys, Sylas Ults, Zhonyas CD, TPs
States: Positioning, Lane State (With Timestamps)
Actions: Crash Wave, Trade
Role-Specific Advice
Factor in unlucky matchmaking
Micro-Mechanics
A way to ask questions to the ai



Week 1:
Explore dataset and figure out how the ai should interpret data (state(hp, level, items, gold, etc)/ action(gank, recall, go to diff lane)/ reward(gold gained, level gained, enemy laner lost gold, objective gained etc, Win/Loss))  finalize decision making schema, pick a few champs and ideally select one role to focus on for now
Self + Team + Enemy States: HP, Level, Items, Unused Gold (Self), Locations, Objectives, CS, Item Difference, KDA, Champion Strength (Respective to Role and Time), Summoner Spells, Jungle Timers, Ults, Item Passives, Vision
Actions: Gank, Roam, Fight, Recall, Farm, Go to objective, Take objective, Push, Freeze, Take turret, Invade, Ward
Rewards(Primary): Win (Desired)/ Loss
A: Practice parsing and understanding the data, mess around and try to see how to get information (EX: How to find where a specific champ is at a given time, or find someone’s gold value at a certain time etc), understand what any important events look like in the data
B: Create a training loop and test with fake data, give it basic situations and see how it responds (create a model and just give it a imaginary situation and see the outcome), make sure the model can take in a state and give an action prediction output (u can look at ur own games as reference) , make sure the loop runs without crashing, and create a way to get a concrete number that reflects accuracy (EX: Comparing to pro gameplay, made 70% of same decision or 30% etc. (Comparing against pro play is only a good first metric, later don’t necessarily use that as reference and probably create an action value measure (what was gained etc.)))



