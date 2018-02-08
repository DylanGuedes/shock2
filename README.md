# SHOCK

* Spark version: 2.2.0
* Written in Scala

# Running

1. Install `docker` and `docker-compose`

2. Run containers:
  `docker-compose up -d`

3. Enter in SBT repl:
  `sbt`

3. Create jars (inside sbt repl):
  `package`

4. Assembly dependencies and binaries (inside sbt repl):
  `assembly`

4. Enter in the Spark Master container
  `docker-compose exec -it shock_master_1 /bin/bash

5. Run the assembly
  `./bin/spark-submit /shock/scala-2.11/shock-assembly-0.0.1.jar

# Troubleshooting

* Permission Error when packaging

Check folders permission via `ls -l`. If target has root as owner, you could
delete it and rerun the packaging.
