## Structure
- ./execs contians executables, for both linux and osx.
- ./configs contains the different configuration files.

## Configs
The config files can be changed, and will allow you to run customize at what blocks specific hardforks trigger. They should be triggered in order, for example Atlantis should not come before the DAO_Hardfork. Hardforks that you do not care to execute can start at block 0, this does not have any negative affects.

## Run
Using Gethc (geth-classic):

`./execs/gethc-<os> --chain ./configs/gethc.json --bootnodes <enode>`
- \<os>: The opperating system you are using (osx, linux)
- \<enode>: The enode address of the client you wish to connect to.

Alterantively, you can omit the `--bootnodes` flag, and capture the enode from gethc. It will appear in the startup logs:
`2019-10-18 15:44:41 UDP listening. Client enode: <ENODE>` and use it on your ethereum client of choice.
