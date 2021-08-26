#FROM 180a51c0/gh-action-buildapp
FROM cornelissenthijs/run-buildapp

COPY entrypoint.sh /entrypoint.sh
RUN chmod 0755 /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
