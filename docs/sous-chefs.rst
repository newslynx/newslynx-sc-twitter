
Sous Chefs
-------------
**newslynx-sc-twitter** provides access to the following Sous Chefs

Twitter List To Event
~~~~~~~~~~~~~~~~~~~~~

-  Extracts events from a twitter list.
-  This Sous Chef runs the python module
   ``newslynx_sc_twitter.events.List``.
-  API Slug: ``twitter-list-to-event``

Development
^^^^^^^^^^^

Pass runtime options to ``twitter-list-to-event`` and stream output.
**NOTE** Will not execute the SousChef's ``load`` method.

.. code:: bash

    $ newslynx sc newslynx_sc_twitter/twitter_list_to_event.yaml option=value1

Alternatively pass in a recipe file

.. code:: bash

    $ newslynx sc newslynx_sc_twitter/twitter_list_to_event.yaml --recipe=recipe.yaml

API Usage
^^^^^^^^^

Add this Sous Chef to your authenticated org

.. code:: bash

    $ newslynx api sous-chefs create -d=newslynx_sc_twitter/twitter_list_to_event.yaml

Create a Recipe with this Sous Chef with command line options.

.. code:: bash

    $ newslynx api recipes create sous_chef=twitter-list-to-event **options

Alternatively pass in a recipe file.

.. code:: bash

    $ newslynx api recipes create sous_chef=twitter-list-to-event --data=recipe.yaml

Save the outputted ``id`` of this recipe, and execute it via the API.
**NOTE** This will place the recipe in a task queue.

.. code:: bash

    $ newslynx api recipes cook id=<id>

Alternatively, run the Recipe, passing in arbitrary runtime options, and
stream it's output: **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: bash

    $ newslynx api recipes cook id=<id> --passthrough **options

Options
^^^^^^^

In addition to default recipe options, ``twitter-list-to-event`` also
accepts the following

-  ``list_owner_screen_name``

   -  **Required**
   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``string``

-  ``list_slug``

   -  **Required**
   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``string``

-  ``min_followers``

   -  Filter out tweets from users with less than X followers.

   -  **Required**
   -  Should be rendered with a ``number`` form.
   -  Accepts inputs of type:

      -  ``numeric``
      -  ``nulltype``

   -  Defaults to ``0``

-  ``search_query``

   -  **Required**
   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``searchstring``
      -  ``nulltype``

   -  Defaults to ``None``

-  ``must_link``

   -  Only create an event if there is a link to an existing content
      item.

   -  **Required**
   -  Should be rendered with a ``checkbox-single`` form.
   -  Choose from:

      -  ``False``

   -  Accepts inputs of type:

      -  ``boolean``

   -  Defaults to ``False``

-  ``event_status``

   -  Set the status of the resulting events. Choose from pending and
      approved. Defaults to pending.

   -  Should be rendered with a ``select`` form.
   -  Choose from:

      -  ``pending``
      -  ``approved``

   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``pending``

-  ``set_event_title``

   -  Set's the title of the resulting events. This can be a python
      format string which has access to all of an event's top-level
      keys: IE: "Content from {authors} at {created}."

   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``None``

-  ``set_event_description``

   -  Set's the description of the output events. This can be a python
      format string which has access to all of an event's top-level
      keys: IE: "{title}."

   -  Should be rendered with a ``paragraph`` form.
   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``None``

-  ``set_event_tag_ids``

   -  A list of Tag IDs or slugs to automatically apply to events
      created by this recipe.

   -  Should be rendered with a ``checkbox`` form.
   -  Choose from:

   -  Accepts inputs of type:

      -  ``string``
      -  ``numeric``

   -  Defaults to ``[]``

-  ``set_event_content_items``

   -  A list of Content Item IDs and Titles to automatically apply to
      events created by this Recipe.

   -  Should be rendered with a ``search`` form.
   -  Choose from:

   -  Accepts inputs of type:

      -  ``json``

   -  Defaults to ``[]``



Search For Links to Content Items
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  This Sous Chef looks up all content items via the API and searches
   Twitter for tweets that links to the same URLs.
-  This Sous Chef runs the python module
   ``newslynx_sc_twitter.events.SearchContentItemLinks``.
-  API Slug: ``twitter-search-content-item-links-to-event``

Development
^^^^^^^^^^^

Pass runtime options to ``twitter-search-content-item-links-to-event``
and stream output. **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: bash

    $ newslynx sc newslynx_sc_twitter/twitter_search_content_item_links_to_event.yaml option=value1

Alternatively pass in a recipe file

.. code:: bash

    $ newslynx sc newslynx_sc_twitter/twitter_search_content_item_links_to_event.yaml --recipe=recipe.yaml

API Usage
^^^^^^^^^

Add this Sous Chef to your authenticated org

.. code:: bash

    $ newslynx api sous-chefs create -d=newslynx_sc_twitter/twitter_search_content_item_links_to_event.yaml

Create a Recipe with this Sous Chef with command line options.

.. code:: bash

    $ newslynx api recipes create sous_chef=twitter-search-content-item-links-to-event **options

Alternatively pass in a recipe file.

.. code:: bash

    $ newslynx api recipes create sous_chef=twitter-search-content-item-links-to-event --data=recipe.yaml

Save the outputted ``id`` of this recipe, and execute it via the API.
**NOTE** This will place the recipe in a task queue.

.. code:: bash

    $ newslynx api recipes cook id=<id>

Alternatively, run the Recipe, passing in arbitrary runtime options, and
stream it's output: **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: bash

    $ newslynx api recipes cook id=<id> --passthrough **options

Options
^^^^^^^

In addition to default recipe options,
``twitter-search-content-item-links-to-event`` also accepts the
following

-  ``must_link``

   -  Only create an event if there is a link to an existing content
      item.

   -  **Required**
   -  Should be rendered with a ``checkbox-single`` form.
   -  Choose from:

      -  ``False``

   -  Accepts inputs of type:

      -  ``boolean``

   -  Defaults to ``False``

-  ``event_status``

   -  Set the status of the resulting events. Choose from pending and
      approved. Defaults to pending.

   -  Should be rendered with a ``select`` form.
   -  Choose from:

      -  ``pending``
      -  ``approved``

   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``pending``

-  ``set_event_title``

   -  Set's the title of the resulting events. This can be a python
      format string which has access to all of an event's top-level
      keys: IE: "Content from {authors} at {created}."

   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``None``

-  ``set_event_description``

   -  Set's the description of the output events. This can be a python
      format string which has access to all of an event's top-level
      keys: IE: "{title}."

   -  Should be rendered with a ``paragraph`` form.
   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``None``

-  ``set_event_tag_ids``

   -  A list of Tag IDs or slugs to automatically apply to events
      created by this recipe.

   -  Should be rendered with a ``checkbox`` form.
   -  Choose from:

   -  Accepts inputs of type:

      -  ``string``
      -  ``numeric``

   -  Defaults to ``[]``

-  ``set_event_content_items``

   -  A list of Content Item IDs and Titles to automatically apply to
      events created by this Recipe.

   -  Should be rendered with a ``search`` form.
   -  Choose from:

   -  Accepts inputs of type:

      -  ``json``

   -  Defaults to ``[]``



Twitter Search To Event
~~~~~~~~~~~~~~~~~~~~~~~

-  Extracts events from a Twitter API query.
-  This Sous Chef runs the python module
   ``newslynx_sc_twitter.events.Search``.
-  API Slug: ``twitter-search-to-event``

Development
^^^^^^^^^^^

Pass runtime options to ``twitter-search-to-event`` and stream output.
**NOTE** Will not execute the SousChef's ``load`` method.

.. code:: bash

    $ newslynx sc newslynx_sc_twitter/twitter_search_to_event.yaml option=value1

Alternatively pass in a recipe file

.. code:: bash

    $ newslynx sc newslynx_sc_twitter/twitter_search_to_event.yaml --recipe=recipe.yaml

API Usage
^^^^^^^^^

Add this Sous Chef to your authenticated org

.. code:: bash

    $ newslynx api sous-chefs create -d=newslynx_sc_twitter/twitter_search_to_event.yaml

Create a Recipe with this Sous Chef with command line options.

.. code:: bash

    $ newslynx api recipes create sous_chef=twitter-search-to-event **options

Alternatively pass in a recipe file.

.. code:: bash

    $ newslynx api recipes create sous_chef=twitter-search-to-event --data=recipe.yaml

Save the outputted ``id`` of this recipe, and execute it via the API.
**NOTE** This will place the recipe in a task queue.

.. code:: bash

    $ newslynx api recipes cook id=<id>

Alternatively, run the Recipe, passing in arbitrary runtime options, and
stream it's output: **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: bash

    $ newslynx api recipes cook id=<id> --passthrough **options

Options
^^^^^^^

In addition to default recipe options, ``twitter-search-to-event`` also
accepts the following

-  ``api_query``

   -  The query to the Twitter API to return the initial batch of
      tweets.

   -  **Required**
   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``string``

   -  More details on this option can be found
      `here <https://dev.twitter.com/rest/public/search>`__

-  ``result_type``

   -  The type of tweets to return from the Twitter API.

   -  **Required**
   -  Should be rendered with a ``select`` form.
   -  Choose from:

      -  ``recent``
      -  ``popular``
      -  ``both``

   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``recent``

   -  More details on this option can be found
      `here <https://dev.twitter.com/rest/public/search>`__

-  ``search_query``

   -  The query we use for additional filtration on text and urls.

   -  **Required**
   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``searchstring``
      -  ``nulltype``

   -  Defaults to ``None``

-  ``min_followers``

   -  Filter out tweets from users with less than X followers.

   -  **Required**
   -  Should be rendered with a ``number`` form.
   -  Accepts inputs of type:

      -  ``numeric``
      -  ``nulltype``

   -  Defaults to ``0``



Twitter User To Event
~~~~~~~~~~~~~~~~~~~~~

-  Extracts events from a twitter user's timeline.
-  This Sous Chef runs the python module
   ``newslynx_sc_twitter.events.User``.
-  API Slug: ``twitter-user-to-event``

Development
^^^^^^^^^^^

Pass runtime options to ``twitter-user-to-event`` and stream output.
**NOTE** Will not execute the SousChef's ``load`` method.

.. code:: bash

    $ newslynx sc newslynx_sc_twitter/twitter_user_to_event.yaml option=value1

Alternatively pass in a recipe file

.. code:: bash

    $ newslynx sc newslynx_sc_twitter/twitter_user_to_event.yaml --recipe=recipe.yaml

API Usage
^^^^^^^^^

Add this Sous Chef to your authenticated org

.. code:: bash

    $ newslynx api sous-chefs create -d=newslynx_sc_twitter/twitter_user_to_event.yaml

Create a Recipe with this Sous Chef with command line options.

.. code:: bash

    $ newslynx api recipes create sous_chef=twitter-user-to-event **options

Alternatively pass in a recipe file.

.. code:: bash

    $ newslynx api recipes create sous_chef=twitter-user-to-event --data=recipe.yaml

Save the outputted ``id`` of this recipe, and execute it via the API.
**NOTE** This will place the recipe in a task queue.

.. code:: bash

    $ newslynx api recipes cook id=<id>

Alternatively, run the Recipe, passing in arbitrary runtime options, and
stream it's output: **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: bash

    $ newslynx api recipes cook id=<id> --passthrough **options

Options
^^^^^^^

In addition to default recipe options, ``twitter-user-to-event`` also
accepts the following

-  ``screen_name``

   -  **Required**
   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``string``

-  ``search_query``

   -  **Required**
   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``searchstring``
      -  ``nulltype``

   -  Defaults to ``None``



Twitter User Timeseries Metrics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Computes a timeseries of of metrics for one or more facebook pages.
-  This Sous Chef runs the python module
   ``newslynx_sc_twitter.metrics.OrgTimeseries``.
-  API Slug: ``twitter-user-to-org-timeseries``

Development
^^^^^^^^^^^

Pass runtime options to ``twitter-user-to-org-timeseries`` and stream
output. **NOTE** Will not execute the SousChef's ``load`` method.

.. code:: bash

    $ newslynx sc newslynx_sc_twitter/twitter_user_to_org_timeseries.yaml option=value1

Alternatively pass in a recipe file

.. code:: bash

    $ newslynx sc newslynx_sc_twitter/twitter_user_to_org_timeseries.yaml --recipe=recipe.yaml

API Usage
^^^^^^^^^

Add this Sous Chef to your authenticated org

.. code:: bash

    $ newslynx api sous-chefs create -d=newslynx_sc_twitter/twitter_user_to_org_timeseries.yaml

Create a Recipe with this Sous Chef with command line options.

.. code:: bash

    $ newslynx api recipes create sous_chef=twitter-user-to-org-timeseries **options

Alternatively pass in a recipe file.

.. code:: bash

    $ newslynx api recipes create sous_chef=twitter-user-to-org-timeseries --data=recipe.yaml

Save the outputted ``id`` of this recipe, and execute it via the API.
**NOTE** This will place the recipe in a task queue.

.. code:: bash

    $ newslynx api recipes cook id=<id>

Alternatively, run the Recipe, passing in arbitrary runtime options, and
stream it's output: **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: bash

    $ newslynx api recipes cook id=<id> --passthrough **options

Options
^^^^^^^

In addition to default recipe options,
``twitter-user-to-org-timeseries`` also accepts the following

-  ``screen_name``

   -  The name of your twitter account.

   -  **Required**
   -  Should be rendered with a ``text`` form.
   -  Accepts inputs of type:

      -  ``string``

Metrics
^^^^^^^

``twitter-user-to-org-timeseries`` generates the following Metrics

-  ``twitter_followers``

   -  Display name: ``Twitter Followers``

   -  Type: ``cumulative``

   -  Org Levels:

      -  ``timeseries``
      -  ``summary``



