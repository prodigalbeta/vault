- digital baseball scoresheet
	- stylized to look like a macintosh system 7 program
	- 2 views
		- Data View
			-  Two descriptive concatenated strings that can be parsed by [[e6_Stats]]
				- strings are wrapped in `inning.atBat("string")`
				- In the rare event of multiple at bats by a single player in one inning, strings will be comma separated
				- On Base
					- (#ofbases)(lettercode s, d, t, h, b, e for how base was reached)(# of RBIs)(.)(total additional bases advanced)(how next base was reached{array of methods}, dot separated)(final result R for run scored, S for stranded, O.(outcode).(out # in inning) for out)
					- ex: `2d2.2s.bR` (on-base double, 2 RBIs, advanced to 3rd with stolen base, walked in to home, resulting in score)
					- ex: `1s0.2S.bO.dp.2` (on-base single, no RBIs, advanced to 2nd with a stolen base, advanced to 3rd on BB, caught out in double play, second out of inning)
				- Out
					- (lettercode for method of out{too many to list right here})(fielders involved in play{1 for K})(.)(out # in inning)
					- ex: `k1.1` (called strike, first out of inning)
					- ex: `TP543.3` (triple play, 3rd baseman to 2nd baseman to 1st baseman, third out of inning)
		- Traditional View
			- More traditional Drawn View

Built around the "atBat" function
```
public func atBat () -> String {
	
}
```

