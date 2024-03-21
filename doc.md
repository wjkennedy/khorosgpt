::: container-fluid
::: row-fluid
::: {#sidenav .span2}
-   [API Summary](#api-_)
-   [API Methods - Search](#api-Search)
-   [searchMessages](#api-Search-searchMessages)
:::

::: {#content}
::: {#project}
::: pull-left
# Simple Atlassian Community Search API
:::

::: clearfix
:::
:::

::: {#header}
::: {#api-_}
## API and SDK Documentation {#welcome-to-apidoc}

::: app-desc
Version: 1.0.0
:::

------------------------------------------------------------------------

<div>

This API allows performing a simple search in the Atlassian Community
messages.

</div>
:::
:::

::: {#sections}
::: {#api-Search .section}
# Search

::: {#api-Search-searchMessages}
::: pull-left
# searchMessages

Search in Atlassian Community messages
:::

::: pull-right
:::

::: clearfix
:::

\

``` {.prettyprint .language-html .prettyprinted data-type="get"}
/search
```

### Usage and SDK Samples

-   [Curl](#examples-Search-searchMessages-0-curl)
-   [Java](#examples-Search-searchMessages-0-java)
-   [Android](#examples-Search-searchMessages-0-android)
-   [Obj-C](#examples-Search-searchMessages-0-objc)
-   [JavaScript](#examples-Search-searchMessages-0-javascript)
-   [C#](#examples-Search-searchMessages-0-csharp)
-   [PHP](#examples-Search-searchMessages-0-php)
-   [Perl](#examples-Search-searchMessages-0-perl)
-   [Python](#examples-Search-searchMessages-0-python)

::: tab-content
::: {#examples-Search-searchMessages-0-curl .tab-pane .active}
``` prettyprint
curl -X GET\
-H "Accept: application/json"\
"https://virtserver.swaggerhub.com/WILLIAM_25/Community/1.0.0/search?q="
```
:::

::: {#examples-Search-searchMessages-0-java .tab-pane}
``` prettyprint
import io.swagger.client.*;
import io.swagger.client.auth.*;
import io.swagger.client.model.*;
import io.swagger.client.api.SearchApi;

import java.io.File;
import java.util.*;

public class SearchApiExample {

    public static void main(String[] args) {
        
        SearchApi apiInstance = new SearchApi();
        String q = q_example; // String | SQL-like query to search messages. Supports filtering by tags, conversation style, replies count, and depth.
Allows ordering and limiting the number of results.

        try {
            inline_response_200 result = apiInstance.searchMessages(q);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling SearchApi#searchMessages");
            e.printStackTrace();
        }
    }
}
```
:::

::: {#examples-Search-searchMessages-0-android .tab-pane}
``` prettyprint
import io.swagger.client.api.SearchApi;

public class SearchApiExample {

    public static void main(String[] args) {
        SearchApi apiInstance = new SearchApi();
        String q = q_example; // String | SQL-like query to search messages. Supports filtering by tags, conversation style, replies count, and depth.
Allows ordering and limiting the number of results.

        try {
            inline_response_200 result = apiInstance.searchMessages(q);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling SearchApi#searchMessages");
            e.printStackTrace();
        }
    }
}
```
:::

::: {#examples-Search-searchMessages-0-objc .tab-pane}
``` prettyprint
String *q = q_example; // SQL-like query to search messages. Supports filtering by tags, conversation style, replies count, and depth.
Allows ordering and limiting the number of results.


SearchApi *apiInstance = [[SearchApi alloc] init];

// Search in Atlassian Community messages
[apiInstance searchMessagesWith:q
              completionHandler: ^(inline_response_200 output, NSError* error) {
                            if (output) {
                                NSLog(@"%@", output);
                            }
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];
```
:::

::: {#examples-Search-searchMessages-0-javascript .tab-pane}
``` prettyprint
var SimpleAtlassianCommunitySearchApi = require('simple_atlassian_community_search_api');

var api = new SimpleAtlassianCommunitySearchApi.SearchApi()
var q = q_example; // {{String}} SQL-like query to search messages. Supports filtering by tags, conversation style, replies count, and depth.
Allows ordering and limiting the number of results.


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.searchMessages(q, callback);
```
:::

::: {#examples-Search-searchMessages-0-csharp .tab-pane}
``` prettyprint
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class searchMessagesExample
    {
        public void main()
        {

            var apiInstance = new SearchApi();
            var q = q_example;  // String | SQL-like query to search messages. Supports filtering by tags, conversation style, replies count, and depth.
Allows ordering and limiting the number of results.


            try
            {
                // Search in Atlassian Community messages
                inline_response_200 result = apiInstance.searchMessages(q);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling SearchApi.searchMessages: " + e.Message );
            }
        }
    }
}
```
:::

::: {#examples-Search-searchMessages-0-php .tab-pane}
``` prettyprint
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\ApiSearchApi();
$q = q_example; // String | SQL-like query to search messages. Supports filtering by tags, conversation style, replies count, and depth.
Allows ordering and limiting the number of results.


try {
    $result = $api_instance->searchMessages($q);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->searchMessages: ', $e->getMessage(), PHP_EOL;
}
?>
```
:::

::: {#examples-Search-searchMessages-0-perl .tab-pane}
``` prettyprint
use Data::Dumper;
use WWW::SwaggerClient::Configuration;
use WWW::SwaggerClient::SearchApi;

my $api_instance = WWW::SwaggerClient::SearchApi->new();
my $q = q_example; # String | SQL-like query to search messages. Supports filtering by tags, conversation style, replies count, and depth.
Allows ordering and limiting the number of results.


eval { 
    my $result = $api_instance->searchMessages(q => $q);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SearchApi->searchMessages: $@\n";
}
```
:::

::: {#examples-Search-searchMessages-0-python .tab-pane}
``` prettyprint
from __future__ import print_statement
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = swagger_client.SearchApi()
q = q_example # String | SQL-like query to search messages. Supports filtering by tags, conversation style, replies count, and depth.
Allows ordering and limiting the number of results.


try: 
    # Search in Atlassian Community messages
    api_response = api_instance.search_messages(q)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling SearchApi->searchMessages: %s\n" % e)
```
:::
:::

## Parameters

::: methodsubtabletitle
Query parameters
:::

+-----------------------------------+-----------------------------------+
| Name                              | Description                       |
+===================================+===================================+
| q\*                               | ::: {#d2e199_searchMessages_q}    |
|                                   | ::: json-schema-view              |
|                                   | ::: primitive                     |
|                                   | [ String ]{.type}                 |
|                                   |                                   |
|                                   | ::: {.inner .description}         |
|                                   | SQL-like query to search          |
|                                   | messages. Supports filtering by   |
|                                   | tags, conversation style, replies |
|                                   | count, and depth. Allows ordering |
|                                   | and limiting the number of        |
|                                   | results.                          |
|                                   | :::                               |
|                                   | :::                               |
|                                   |                                   |
|                                   | ::: {.inner .required}            |
|                                   | Required                          |
|                                   | :::                               |
|                                   | :::                               |
|                                   | :::                               |
+-----------------------------------+-----------------------------------+

## Responses

### Status: 200 - A list of messages matching the query.

-   [Schema](#responses-searchMessages-200-schema){toggle="tab"}

::: {.tab-content style="margin-bottom: 10px;"}
::: {#responses-searchMessages-200-schema .tab-pane .active}
::: {#responses-searchMessages-200-schema-200 style="padding: 30px; border-left: 1px solid #eee; border-right: 1px solid #eee; border-bottom: 1px solid #eee;"}
:::
:::
:::
:::

------------------------------------------------------------------------
:::
:::

::: {#footer}
::: {#api-_footer}
Suggestions, contact, support and error reporting;

::: app-desc
Information URL: <https://helloreverb.com>
:::

::: app-desc
Contact Info: [hello@helloreverb.com](hello@helloreverb.com)
:::

::: license-info
All rights reserved
:::

::: license-url
http://apache.org/licenses/LICENSE-2.0.html
:::
:::
:::
:::
:::
:::
