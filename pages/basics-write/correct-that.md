# correct that

The knausj talon command set (the most widely used community command set) has the following commands for dealing with homophones: https://github.com/knausj85/knausj_talon/blob/main/core/homophones/homophones.talon, https://github.com/knausj85/knausj_talon/blob/main/core/homophones/homophones_open.talon




I modified my dictation mode setup so that I could use the homophone commands from dictation mode

￼

My custom dictation setup is here if you want to borrow anything from it: https://github.com/FireChickenProductivity/TalonVoiceDictationSetup


words_to_replace only replaces a word if it would have otherwise been recognized.
additional_words adds entirely new vocab, which doesn't need to already exist, and increases its priority

When working with visual studio code, I can use cursorless commands to quickly navigate, which is handy for fixing misrecognitions

Some people consequently do their dictation with VSCode instead of something like word and then have a command for copying it to the program where they need it

My custom setup relies on using the talon draft window, which lets me quickly move the cursor and delete words. I have it set up so that I can bring up the homophone menu using the draft window word anchors.

I do have a simple thrown together in a hurry correction system that does little more than fix homophones but it has quite a few bugs. I still find it useful, though. Also, you can customize the homophones system using knausj command "customize homophones", which brings up a csv file.

With the standard knausj set up, you can replace words with the words to replace file (you open it by saying "customize words to replace"). The replacements are permanent, but can be useful for common misrecognitions if you are fine with manually spelling out the replaced words when occasionally needed. As an example, here's the stuff in my words to replace file:

Replacement,Original
January,january
February,february
April,april
June,june
July,july
August,august
September,september
October,october
November,november
December,december
get,git
edit,adit
",",coma
learned,Learned
kernel,colonel
the,thee
in,en
queue,cu
the,THEE

I find misrecognitions where an extra character gets added relatively common, so having a dictation mode command for trimming a letter off of the specified word (either in the draft window or using cursorless with VSCode) can be very handy (things like too instead of to). I'm not sure if that is a common experience or not

I find that conformer often depends on context to understand what you are saying more than dragon, so dictating more words at a time can help

You can use a talon file to adjust how long you have to pause before it figures out you have stopped talking and runs the command. I find that making it significantly longer in dictation mode than in command mode leads to a better experience

+1 on switching from Dragon/Vocola. I used it as my first accessibility voice system when I worked on Windows and Talon at the time was not available for the OS. At first I continued to use Dragon as the speech recognition model due to it being a good bit better for dictation, but after starting to use Cursorless (#ext-cursorless) for both coding and editing long dictation the advantages of using Conformer as well outweighed any of Dragon’s. Add on sound recognition with Parrot and eye tracking, Dragon falls far behind.