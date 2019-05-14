C-----------------------------------------------------------------------
C  			euclidRhythmTester                  
C-----------------------------------------------------------------------
C
C  This pd patch creates "generative music" in conjunction with a Elektron 
C  Digitakt synthesizer.
C
C  It uses Euclidian rhythms as described here: 
C     cgm.cs.mcgill.ca/~godfried/publications/banff.pdf
C  to create afro-cuban sounding rhythms on the Digitakt synthesizer.
C
C  Pure Data sends a midi clock out to the Digitakt and bangs out the Euclidian 
C  rhythms. The Pure Data patch maps these rhythms onto randomly generated notes
C  creating a musical sounding percussion.
C
C  The Digitakt synthesizes the percussive sounds from Buchla drum samples 
C  obtained from here:
C  https://www.synthtopia.com/content/2016/10/03/free-drum-sample-library-features-buchla-music-easel-synthesized-percussion/
C
C  Please see https://youtu.be/7myFyhvJEYg for an example of it's use.
C
C-----------------------------------------------------------------------
C  Requirements:   Pure Data <https://puredata.info/downloads/pure-data>
C-----------------------------------------------------------------------
C
Usage:  The file euclidRhythmTester.pd is the parent patch which contains the 
        rest of the modules.

               Explanation of the primary patches:
midiClockOut:  Sends the midi clock from the Pure Data to the Digitakt at 1/96th note
               intervals.  Provides the euclidRhythm patch with 1/16th note intervals.
euclidRhythm:  Bangs out a randomly varying euclidian rhythm.  This patch uses the 
               patches eSeq, euclidR, expDist, and setctl.
randScales:    This patch maps the percussive bangs onto particular scales in a random
               fashion.

Contributions: Any contributions to this project are welcome.

Acknowledgements: I'd like to thank Acreil for sharing his Pure Data patches. Namely; 
                  pois, rseq, and euclid, to create Euclidian rhythm patches used here.


