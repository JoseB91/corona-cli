Feature to create a csv file

The issue (feature)

The issue can be found at https://github.com/ahmadawais/corona-cli/issues/103. This is a new feature which was ideated from one of the contributors and the owner requested this change to be made as a nice to have feature. Hence we implemented this option to create a csv file with the data which is currently visualized as charts and tables.

Requirements

As a user, I want to be able to extract the output data to csv format after a specific search that I performed.


Design of the fix

This is an additional feature to create a csv file from the command line.It is now added along with the existing chart display feature, so when the user inputs the command to view the states in form of chart, the data is extracted to a csv file.


Source code files

Code changes made on the following files for this feature
utils/getStates.js: the code for extracting state data for visualizing on the application

Add source code

The csv-writer package from npm library is installed in the project. The data is fetched from below api : https://corona.lmao.ninja/v2/states

The data fetched is then formatted to required format. Now the data is mapped to each column for csv generation. A path is also defined inside the project path named /output. The code changes are made in the line number visible in below screenshot.
 
Line number 9: Installed package is imported inside the project
Line number 54 - 64: Data is mapped to required csv format
Line number 66: Write the records to csv file



Submit the fix

A pull request was submitted on the project’s Github and can be found at https://github.com/ahmadawais/corona-cli/pull/103. We have tested the feature in multiple platforms such as macOS, Windows.
