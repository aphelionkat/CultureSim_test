## IMPORTANT ##
On Macs, and potentially other operating systems, this program must be run using Java 8. Newer versions of Java may cause errors when generating surface plots. Java 11 was confirmed to not work.


Run template:
java -jar CultureSim.jar -c <configFileName.json> [-options]

The "-c <configFileName.json>" is a required argument. The "-c" stands for config, and the filename of the desired config file must come immediately after, separated by a space.

After specifying the config file, the user may optionally specify which plots to output. The plots are represented by single characters, which can each individually follow a '-' character, or all follow a single '-' character. The possible letters and their corresponding plots are specified below.

 -f         Output average fitness plot
 -g         Output average gene fitness plot
 -m         Output food plot
 -p         Output population plot
 -s         Output surface plot

Users may also save and load ending populations from simulations. To save:

 -e         Save ending population

To load a population, include "-l <path\to\endingPopulation.ser>".

After the simulation has finished, the plots and raw data are output to a folder named after the type of simulation (chemostat or turbidostat) followed by a date/timestamp.

Basic run example:
java -jar CultureSim.jar -c turbidoConfig.json

Output surface plot and average gene fitness plot:
java -jar CultureSim.jar -c turbidoConfig.json -s -g

Output food and population plots:
java -jar CultureSim.jar -c turbidoConfig.json -m -p

Output food, average fitness, average gene fitness, surface and population plots:
java -jar CultureSim.jar -c turbidoConfig.json -mpsgf

Load ending population from a previous simulation and save ending population:
java -jar CultureSim.jar -c turbidoConfig.json -l turbidostat2020-04-14-00-15-57\endingPopulation.ser -e


Output help message:
java -jar CultureSim.jar -h
