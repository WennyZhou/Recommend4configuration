# Recommend4configuration

## Data-Recommendation for Customized Product Configuration Design

The dataset is designed and developed for the elevator traction machine instance recommendation based on the historical customer¡¯s order and corresponding configuration design scheme.The elevator traction machine instances are the configuration design result of this component. The data contains the traction machine configuration result of 61 different types of elevators.

For the retrieval task, the retrieval dataset is designed and developed. Each record in this dataset is a query-candidate pair. A query (customer requirements) contains 9 numerical feature fields and 8 categorical feature fields, and a candidate (elevator traction machine component instance) contains 3 categorical features (manufacturer, model, and instance identification of the elevator traction machine).

For the ranking task, the ranking dataset is designed and developed. Each record consists of the user¡¯s query, the candidate information, and the adoption score. The feature fields of the user¡¯s query and the candidate information are the same as the retrieval dataset. The adoption scores of positive samples are equal to 1, and the adoption scores of negative samples are equal to 0. For the elevator traction machine instance recommendation, the value range of the adoption score is [0,1], indicating the probability that the user selects the instance candidate as the elevator traction machine configuration design result.

FILES:

The retrieval.txt file contains QUERY-CANDIDATE pairs in the following format:

		<Feature Fields of QUERY> + <Feature Field of CCANDIDATE>

The ranking-1.txt file contains positive samples of the ranking dataset. The adoption score of each sample is 1. 

The ranking-2.txt file contains negative samples of the ranking dataset. The adoption score of each sample is 0. 

Each line in the ranking-1.txt file or the ranking-2.txt file describes a sample in the following format:

		<Adoption Score> <Feature Fields of Customer Requirements and Component Instance Information>

FEATURE FIELDS:

The description of the feature fields in the following format:

		<feature symbol>: <category> <value type> <description>

A query (customer requirement) contains the following feature fields:

<q>: <numerical feature> <integer> <rated load of the elevator>

<v>: <numerical feature> <float> <rated velocity of the elevator>

<v1>: <numerical feature> <float> <actual operating velocity of the elevator>

<p1>: <numerical feature> <float> <power of the elevator traction machine>

<i1>: <numerical feature> <float> <rating current of the electromotor>

<d1>: <numerical feature> <integer> <diameter of traction rope of the elevator>

<n1>: <numerical feature> <integer> <number of rope grooves of the elevator traction sheave>

<yylzj>: <numerical feature> <integer> <diameter of the elevator traction sheave>

<jk>: <numerical feature> <integer> <width of the elevator car>

<bpqlx>: <categorical feature> <string> <type of the frequency converter of the elevator>

<dzklx>: <categorical feature> <string> <type of the counterweight of the elevator>

<qdfs>: <categorical feature> <string> <driving method of the elevator>

<standard>: <categorical feature> <string> <executive standard for the elevator design>

<t_cplx>: <categorical feature> <string> <elevator type>

<u1>: <categorical feature> <string> <braking voltage>

<yyb>: <categorical feature> <string> <traction ratio of the elevator>

<yyjlx>: <categorical feature> <string> <motor type of the elevator>

A candidate (elevator traction machine instance) contains the following feature fields:

<yyjcj>: <categorical feature> <string> <manufacturer of the elevator traction machine>

<yyjxh>: <categorical feature> <string> <model/type of the elevator traction machine>

<item>: <categorical feature> <string> <instance identification of the elevator traction machine>
