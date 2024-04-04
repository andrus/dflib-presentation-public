# DataFrame: a Swiss Army Knife of Java Data Processing
_presentation notebook code_

## Git Notes
After clone, run this to ensure IPython notebooks are committed without output data:
```shell
git config --local include.path ../.gitconfig
```

## Notebook instructions

1. Start Postgres in Docker. This creates a new DB and loads the demo schema.

```shell
docker-compose -f env/docker-compose.yml up -d
```

2. Clear Jupyter Java Dependency Cache. This step is needed until the [following issue is fixed](https://github.com/SpencerPark/IJava/issues/63#issuecomment-2010273926) in the iJava kernel.

```shell
rm -rf ~/.ivy2/
```

3. Run Jupyter

```shell
cd notebooks/
jupyter lab
```

4. When finished, stop Postgres Docker

```shell
docker-compose -f env/docker-compose.yml down --volumes
```