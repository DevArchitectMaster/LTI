# LTI-Schnittstelle



### Konfiguration im LMS

Die Konfiguration im Modul-Menü des jeweiligen LMS wie im Bild beschrieben:
![Konfiguration][configuration]



##### Konfigurationsmöglichkeiten

* **Vorkonfiguriertes Tool**: xxx
* **Tool-URL**: xxx
* **Sichere Tool-URL**: xxx
* **Startcontainer**: xxx
* **Anwenderschlüssel**: xxx
* **Öffentliches Kennwort**: xxx
* **Angepasste Parameter**: xxx
* **Icon URL**: xxx
* **Sichere Icon URL**: xxx



### Paramter & Datenschutz-Einstellungen

Bei den Datenschutz-Einstellungen gibt es drei wählbare Optionen:

* **Anwendername an Tool übergeben**
```json
"lis_person_name_given": "Max",
"lis_person_name_family": "Mustermann",
"lis_person_name_full": "Max Mustermann",
"ext_user_username": "mmustermann",
```

* **E-Mail des Anwenders an Tool übergeben**
```json
"lis_person_contact_email_primary": "max.mustermann@moodle.de",
```

* **Bewertungen aus dem Tool akzeptieren**
```json
"lis_result_sourcedid": "{\"data\":{\"instanceid\":\"1\",\"userid\":\"1993\",\"typeid\":null,\"launchid\":698939916},\"hash\":\"9953feede6d340896d656ad5548f8426fa6b0290dfa2d57da14e2f18d3388125\"}",
"lis_outcome_service_url": "https://moodle.de/mod/lti/service.php",
```

![Datenschutz-Einstellungen][privacy]



### Paramter

Folgende Parameter werden immer an das externe Tool übertragen:

```json
Request Body:
{ 
  "oauth_version": "1.0",
  "oauth_nonce": "9ab92df43500cb4c1090c02592546546",
  "oauth_timestamp": "1547040436",
  "oauth_consumer_key": "key",
  "user_id": "1993",
  "lis_person_sourcedid": "",
  "roles": "Learner",
  "context_id": "4711",
  "context_label": "[LTIP]",
  "context_title": "LTI Project",
  "resource_link_title": "click here",
  "resource_link_description": "",
  "resource_link_id": "1",
  "context_type": "CourseSection",
  "lis_course_section_sourcedid": "",
  "launch_presentation_locale": "de",
  "ext_lms": "moodle-2",
  "tool_consumer_info_product_family_code": "moodle",
  "tool_consumer_info_version": "2017111301.05",
  "oauth_callback": "about:blank",
  "lti_version": "LTI-1p0",
  "lti_message_type": "basic-lti-launch-request",
  "tool_consumer_instance_guid": "moodle.de",
  "tool_consumer_instance_name": "moodle.de",
  "tool_consumer_instance_description": "Moodle",
  "launch_presentation_document_target": "window",
  "launch_presentation_return_url": "https://moodle.de/mod/lti/return.php?course=4711&launch_container=4&instanceid=1&sesskey=Vox4GqE6sv",
  "oauth_signature_method": "HMAC-SHA1",
  "oauth_signature": "bUR1n3fhCgIgw8CQrbRyKZfWSZM=" 
}
```


##### alle möglichen Parameter

```json
Request Body:
{ 
  "oauth_version": "1.0",
  "oauth_nonce": "9ab92df43500cb4c1090c02592546546",
  "oauth_timestamp": "1547040436",
  "oauth_consumer_key": "key",
  "user_id": "1993",
  "lis_person_sourcedid": "",
  "roles": "Learner",
  "context_id": "4711",
  "context_label": "[LTIP]",
  "context_title": "LTI Project",
  "resource_link_title": "click here",
  "resource_link_description": "",
  "resource_link_id": "1",
  "context_type": "CourseSection",
  "lis_course_section_sourcedid": "",
  "lis_result_sourcedid:" [<Bewertungen aus dem Tool akzeptieren>],
  "lis_outcome_service_url": [<Bewertungen aus dem Tool akzeptieren>],
  "lis_person_name_given": [<Bewertungen aus dem Tool akzeptieren>],
  "lis_person_name_family": [<Bewertungen aus dem Tool akzeptieren>],
  "lis_person_name_full": [<Bewertungen aus dem Tool akzeptieren>],
  "ext_user_username": [<Bewertungen aus dem Tool akzeptieren>],
  "lis_person_contact_email_primary": [<E-Mail des Anwenders an Tool übergeben>],
  "launch_presentation_locale": "de",
  "ext_lms": "moodle-2",
  "tool_consumer_info_product_family_code": "moodle",
  "tool_consumer_info_version": "2017111301.05",
  "oauth_callback": "about:blank",
  "lti_version": "LTI-1p0",
  "lti_message_type": "basic-lti-launch-request",
  "tool_consumer_instance_guid": "moodle.de",
  "tool_consumer_instance_name": "moodle.de",
  "tool_consumer_instance_description": "Moodle",
  "launch_presentation_document_target": "window",
  "launch_presentation_return_url": "https://moodle.de/mod/lti/return.php?course=4711&launch_container=4&instanceid=1&sesskey=Vox4GqE6sv",
  "oauth_signature_method": "HMAC-SHA1",
  "oauth_signature": "bUR1n3fhCgIgw8CQrbRyKZfWSZM=" 
}
```



##### alle möglichen Parameter

```json
Request Body:
{ 
  "oauth_version": "1.0",
  "oauth_nonce": "9ab92df43500cb4c1090c02592546546",
  "oauth_timestamp": "1547040436",
  "oauth_consumer_key": "key",
  "user_id": "1993",
  "lis_person_sourcedid": "",
  "roles": "Learner",
  "context_id": "4711",
  "context_label": "[LTIP]",
  "context_title": "LTI Project",
  "resource_link_title": "click here",
  "resource_link_description": "",
  "resource_link_id": "1",
  "context_type": "CourseSection",
  "lis_course_section_sourcedid": "",
  "lis_result_sourcedid:" "{"data":{"instanceid":"1","userid":"1993","typeid":null,"launchid":698939916},"hash":"9953feede6d340896d656ad5548f8426fa6b0290dfa2d57da14e2f18d3388125"}",
  "lis_outcome_service_url": "https://moodle.de/mod/lti/service.php",
  "lis_person_name_given": "Max",
  "lis_person_name_family": "Mustermann",
  "lis_person_name_full": "Max Mustermann",
  "ext_user_username": "mmustermann",
  "lis_person_contact_email_primary": "max.mustermann@moodle.de",
  "launch_presentation_locale": "de",
  "ext_lms": "moodle-2",
  "tool_consumer_info_product_family_code": "moodle",
  "tool_consumer_info_version": "2017111301.05",
  "oauth_callback": "about:blank",
  "lti_version": "LTI-1p0",
  "lti_message_type": "basic-lti-launch-request",
  "tool_consumer_instance_guid": "moodle.de",
  "tool_consumer_instance_name": "moodle.de",
  "tool_consumer_instance_description": "Moodle",
  "launch_presentation_document_target": "window",
  "launch_presentation_return_url": "https://moodle.de/mod/lti/return.php?course=4711&launch_container=4&instanceid=1&sesskey=Vox4GqE6sv",
  "oauth_signature_method": "HMAC-SHA1",
  "oauth_signature": "bUR1n3fhCgIgw8CQrbRyKZfWSZM=" 
}
```





[configuration]: params_img/configuration.png "Konfiguration"
[privacy]: params_img/privacy.png "Datenschutz-Einstellungen"
