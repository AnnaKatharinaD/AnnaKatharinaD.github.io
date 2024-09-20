# How to detect and classify sexist memes with AI

"Am I overreacting and this is just a joke or is it actually sexist?" Most women in online spaces have probably come across a meme or two
that just *feels* vaguely sexist. Personally, I've never been a big fan of the "boy's locker room" type of memes. Basically the boy's locker room is characterized as a place of exciting chaos,
while the girls set up the punchline by being annoyed that P.E. is messing up their hair and makeup, gossiping about cute boys or each other.
In a world where memes can be funny, biting, or outright harmful, how do we teach machines to tell the difference?
Enter SemEval-2022’s Misogyny Classification Challenge, where researchers tackled the task of detecting misogyny in memes.
Our team took on the challenge by developing two models: one that uses both images and text, and another that works on text alone.

For simple detection, we built an ensemble of classifiers that analyzed meme images and accompanying text.
It could spot harmful content by looking for signs like nudity, gender imbalance, and negative sentiment.
We ranked 5th on the leaderboard with an F1-score of 0.665!
For the more complex task—identifying specific misogynistic themes
like shaming or objectification we used RoBERTa, a transformer model trained on text, landing in 19th place.
