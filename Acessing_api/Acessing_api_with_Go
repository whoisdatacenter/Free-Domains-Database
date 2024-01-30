// Go
package main

import (
"encoding/json"
"fmt"
"io/ioutil"
"net/http"
)

func main() {
apiKey := "place_your_api_key_here"
domain := "example.com"
apiURL := fmt.Sprintf("https://api.whoisdatacenter.com/v1/domain?apiKey=%s&domain=%s", apiKey, domain)

response, err := http.Get(apiURL)
if err != nil {
panic(err)
}
defer response.Body.Close()

body, err := ioutil.ReadAll(response.Body)
if err != nil {
panic(err)
}

var data map[string]interface{}
err = json.Unmarshal(body, &data)
if err != nil {
panic(err)
}

fmt.Println(data)
}
