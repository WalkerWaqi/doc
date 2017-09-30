* key

  ```
  init0
  [{"private_key":"5KVDrKgX3fx9SADYQzQGAQaxwC2pmArpTg9YVNRBhi6v9KttNRr","public_key":"BTS63eu28enwUaq4anKTaD4JmezYdaBK3rGQj887K4cwk9XBvTFkY","address":"BTSCHmLyXhKJhFxtCspWiSrLD48B9HfGMFA9"}]

  www
  suggest_brain_key
  {
    "brain_priv_key": "VACUATE ORCIN BANDAGE LARVATE CUBBISH COOKERY BORT PARTO PARISON PAWNAGE WORMING SCALAR JETTY GRIMY PLAKAT SACRED",
    "wif_priv_key": "5KRCnbiQni6uovyyBJj4qUrVRRJhKBZnMyv9XD149guDss3z9bf",
    "pub_key": "BTS5QWQ4dw38ureGWDxPKhrGXKupi9batWFiXC7G3BEfAS2iPzKLy"
  }
  ```

* witness_node

  ```
  ./witness_node --data-dir data
  ```

* cli_wallet

  ```
  ./cli_wallet --wallet-file=my-wallet.json --chain-id 178c044c62ada670e29e820a2e220bec1d4cdf3630d50a569718a2f4f3ba7970 --server-rpc-endpoint=ws://118.190.159.23:11011

  import_key init0 5KVDrKgX3fx9SADYQzQGAQaxwC2pmArpTg9YVNRBhi6v9KttNRr

  import_balance init0 ["5KVDrKgX3fx9SADYQzQGAQaxwC2pmArpTg9YVNRBhi6v9KttNRrlist"] true

  get_account init0

  list_account_balances init0

  transfer init0 www 500 BTS "here is some cash" true

  create_account_with_brain_key "Brain ... key" <accountname> init0 init0 true

  reserve_asset init0 100 BTS true
  fund_asset_fee_pool init0 BTS 100 true

  vote_for_committee_member init2 init2 true true

  propose_parameter_change init0 "20171019T133030"  {"block_interval" : 10} true
  approve_proposal init0 1.10.0 {"active_approvals_to_add" : ["init0"]} true
  approve_proposal init1 1.10.0 {"active_approvals_to_add" : ["init1"]} true
  approve_proposal init2 1.10.0 {"active_approvals_to_add" : ["init2"]} true

  propose_parameter_change init0 "20171019T133030" {"block_interval" : 20} true
  propose_fee_change init0 "20170930T052800" { 0 : { "fee" : 200000, "price_per_kbyte" : 0 } } true
  approve_proposal init0 "1.10.0" {"active_approvals_to_add" : ["test2"]} true
  ```


