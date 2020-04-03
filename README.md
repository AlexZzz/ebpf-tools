# ebpf-tools
This repo contains some eBPF-based tools for tracing.

## make_request_lat
Summarizes `generic_make_request()` latency as a histogramm.

## make_request_slower
Shows `generic_make_request()` calls which were slower than expected. Usefull to find out when kernel submits requests slowly. Possible reasons are: a lot of `blk_mq_queue_freeze()` calls or slow `generic_make_request_checks()`.
