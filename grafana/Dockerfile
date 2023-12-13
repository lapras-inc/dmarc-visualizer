FROM grafana/grafana:8.5.4

ADD --chown=grafana:root https://raw.githubusercontent.com/domainaware/parsedmarc/master/grafana/Grafana-DMARC_Reports.json /var/lib/grafana/dashboards/
# https://github.com/domainaware/parsedmarc/issues/356#issuecomment-1571222598
RUN sed -i 's/fixed_interval/interval/g' /var/lib/grafana/dashboards/Grafana-DMARC_Reports.json
RUN chmod 644 /etc/grafana/provisioning

COPY grafana-provisioning/ /etc/grafana/provisioning/
