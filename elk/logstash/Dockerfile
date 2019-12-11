# https://github.com/elastic/logstash-docker
FROM logstash:6.8.3
COPY ./config/logstash.yml /usr/share/logstash/config/logstash.yml
COPY ./pipeline/ /usr/share/logstash/pipeline/
# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json
RUN sed -i 's/rubygems.org/gems.ruby-china.com/g' Gemfile
RUN logstash-plugin install logstash-input-http