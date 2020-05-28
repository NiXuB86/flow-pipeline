#FROM ubuntu AS builder

#RUN apt-get update && apt-get install -y git
#RUN git clone https://github.com/Vertamedia/clickhouse-grafana.git

FROM grafana/grafana

#COPY --from=builder /clickhouse-grafana /var/lib/grafana/plugins/clickhouse-grafana

RUN grafana-cli plugins install vertamedia-clickhouse-datasource && grafana-cli plugins install grafana-piechart-panel && grafana-cli plugins install grafana-clock-panel && grafana-cli plugins install grafana-simple-json-datasource && grafana-cli plugins install grafana-worldmap-panel
#RUN grafana-cli plugins install grafana-clock-panel
#RUN grafana-cli plugins install grafana-simple-json-datasource
#RUN grafana-cli plugins install grafana-worldmap-panel

