FROM    gcc AS compilation
COPY    sources /src
WORKDIR /src
RUN     gcc -o prog -static prog.c 

FROM scratch
COPY --from=compilation /src/prog /
CMD  ["/prog"]
