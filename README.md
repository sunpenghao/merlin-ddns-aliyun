# How to Use

Create a type A DNS record of the domain to be resolved in your Aliyun account. The script will update this record automatically when the ISP changes your IP address.

Set the following variables in the script:
* `AccessKeyId` - Your Aliyun Access Key ID
* `Key` - Your Aliyun Access Key Secret plus a "&" character
* `RecordId` - ID of the record to be updated
* `RR` - The script resolves `ddns.example.com` by default; change this if needed

You may need to use Aliyun's API to get the desired `RecordId`. Refer to the API documentation for more information: <https://help.aliyun.com/document_detail/29776.html>

Place the script on your router under `/jffs/scripts`. Remember to grant execution permission:
```sh
chmod +x /jffs/scripts/ddns-start
```

Finally, set DDNS service provider to `custom` in the router's Web UI, and you are ready to go :)
