In two-term mode it is expected that NLE's will be in the form of two terms squared.   To maximize the code in common with three-term mode, two base terms are
squared to generate a synthetic third term and then processed like a three-term NLE.  The relationship between the third term coefficient c3 and the two from
term1 and term2 is called two-term test = c3/(c1*c2).  Only when two-term test = 2 can the NLE be of the form (c1*term1 +/- c2*term2)^2 - 1 = 0 where +/- is the
two-term mixing polarity (sign).

The sample configuration file in this directory and script in ./plot will generate plots of the coefficients and two-term test vs a randomly selected reference
mass in (1-smr) mode.  These graphs can help to understand the behavior of these NLE's and find reference masses/smrfactors where two-term test = 2.  

Use a start script from the /scripts directory to start as many threads as you have vcpu's and save the output to a unique leptonout-*.txt file for each thread.
If you stop and restart (to reconfigure for example), make a run-* (example: ./run-01) subdirectory and move leptonout-* there so you don't lose your existing
data. Similarly you can run threads on multiple remote servers, rsync them to separate run-* directories for increased processing power.   

Then change to the plot subdirectory and execute run.sh to generate .csv files and plots from the output files (requires gnuplot).  It will look for output
files ../leptonout-* and ../run-*/leptonout-*.

The naming convention for the plot files includes the inverse exponents for term1 and term2, the two-term mixing polarity (+ or -), and the mass configuration (M/mr = +M, mr/M = -M).
