# SNEED ICRC-1 Implementation
This repo contains the source code for the SNEED ICRC1 token, 
a fork of the [NatLabs implementation](https://github.com/NatLabs/icrc1) of the 
[ICRC-1](https://github.com/dfinity/ICRC-1) token standard. 

NB: A logo field has been added to the construction arguments. Below is the example from NatLabs, modified to include the logo field.
    
  - Replace the values enclosed in `< >` with your desired values and run in the terminal 

  ```motoko
    git clone https://github.com/icsneed/sneed
    cd sneed
    mops install
    dfx start --background --clean

    dfx deploy icrc1 --argument '( record {                     
        name = "<Insert Token Name>";                         
        symbol = "<Insert Symbol>";                           
        decimals = 6;                                           
        fee = 1_000_000;                                        
        logo = "data:image/png;base64,iVBORw0...K5CYII=";                                        
        max_supply = 1_000_000_000_000;                         
        initial_balances = vec {                                
            record {                                            
                record {                                        
                    owner = principal "<Insert Principal>";   
                    subaccount = null;                          
                };                                              
                100_000_000                                 
            }                                                   
        };                                                      
        min_burn_amount = 10_000;                         
        minting_account = null;                                 
        advanced_settings = null;                               
    })'
  ```

## Funding

This source code was forked from a library that was initially incentivized by [ICDevs](https://icdevs.org/). You can view more about the bounty on the [forum](https://forum.dfinity.org/t/completed-icdevs-org-bounty-26-icrc-1-motoko-up-to-10k/14868/54) or [website](https://icdevs.org/bounties/2022/08/14/ICRC-1-Motoko.html). The bounty was funded by The ICDevs.org community and the DFINITY Foundation and the award was paid to [@NatLabs](https://github.com/NatLabs). If you use this source code or the library it was forked from and gain value from it, please consider a [donation](https://icdevs.org/donations.html) to ICDevs.