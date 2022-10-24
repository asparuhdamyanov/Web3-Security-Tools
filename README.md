# Web3-Security-Tools

Using Smart Contract Security tools for testing sample code

## Echidna

Examples of fuzzing with Echidna.

1. Make sure you've got Docker installed
   https://docs.docker.com/desktop/install/windows-install/ (this is for windows)

2. `cd .\Echidna\contracts\ `

3. `docker run -it --rm -v ${PWD}:/code trailofbits/eth-security-toolbox`

Inside docker, your code will be stored at /code

4. Testing

`echidna-test TestEchidna.sol --test-limit 5000 -- contract TestCounter`

Some of the tests are made to fail on purpose.
Feel free to play Around!

5. If needed you can change solc version

`solc-select 0.7.6`

### Testing Time and Sender

Echidna can fuzz timestamp. Range of timestamp is set in the configuration. Default is 7 days.

Contract callers can also be set in the configuration. Default accounts are

    0x10000
    0x20000
    0x00a329C0648769a73afAC7F9381e08fb43DBEA70

    view TestTimeAndCaller.sol for more.

## Slither

Using Slither static analysis tool.

Update: View real example of using Slither at:
https://github.com/asparuhdamyanov/Space-Cola-Vending-Machine
