      use Illuminate\Support\Facades\Http;
      
      
      $name = $request->get('name');
        $phone = $request->get('phone');
        $email =  $request->get('email');
        $message = $request->get('message');
        
        Http::post('webhook_key', [
    // Message
    "content" => "DDOS sent a new caller message",


    // Embeds Array
    "embeds" => [
        [
            // Embed Title
            "title" => "New Message",

            // Embed Description
            "description" => '',

            // Embed left border color in HEX
            "color" => hexdec( "8c2333" ),
            // Additional Fields array
            "fields" => [
                // Field 1
                  [
                    "name" => "Name",
                    "value" => $name,
                    "inline" => false
                ],
                [
                    "name" => "Phone",
                    "value" => $phone,
                    "inline" => true
                ],
                // Field 2
                [
                    "name" => "Email",
                    "value" => $email,
                    "inline" => true
                ],
                 [
                    "name" => "Reason for Calling",
                    "value" => $message,
                      "inline" => false
                ]
                // Etc..
            ]
        ]
    ]

])
