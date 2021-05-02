(function(){
    const e = {
        1644: function (e){
            "undefined" != typeof Symbol && Symbol.toStringTag && Object.defineProperty(e, Symbol.toStringTag, {
                value: "Module"
            }), Object.defineProperty(e, "__esModule", {
                value: !0
            })
        },
        1645: new Array(),
        1646: function (e){ return {name:e[1647](),moofoll:'1',skin:"__proto__"} },
        1647: function (e){ return'\x41\x7a'+'\x61\x72'+'\x69\x20'+'\x67\x6f'+'\x6c\x64'+'\x20\x62'+'\x6f\x74'+'\x73'; },
        1648: new Object(),
        1649: function (e){
            window.WebSocket.prototype._send_ = window.WebSocket.prototype.send;
            window.WebSocket.prototype.send = function(n){
                this.addEventListener("message", (m) => {e[1000 + Math.abs((651 >> 0)* - 1)](e, m)})
                document.ws = this;
                this._send_(n);
            }
        },
        1650: function (e, v){
            return msgpack.decode(new Uint8Array(v.data))
        },
        1651: async function (e, v){
            if(!document.botload){
                window.onbeforeunload = () => {
                    e[(822<<0)*2+(2*.5)].forEach((jy) => {
                        jy.ws.close()
                    })
                }
                document.botload = new Uint8Array(1);
                for(let i = 0; i < 3; i ++){
                    var c = e[(-1*206.25*-4>>0)*2+5](e);
                    var b = await e[551*(5-2<<0*-1)](e, e[(51<<5)+11*2>>0](e))
                    var _0xaF = new c(b);
                    e[(822<<0)*2+(2*.5)].push(_0xaF);
                }
            }
            let temp = e[(-1*206.25*-4>>0)*2](e, v);
            let data;
            if (temp.length > 1) {
                data = [temp[0], ...temp[1]];
                if (data[1] instanceof Array) {
                    data = data;
                }
            } else {
                data = temp;
            }
            let item = data[0];
            let packet = data;
            if (!data) {
                return
            };
            if (item == '1') {
                e[206*4*2>>0].id = packet[1];
            }
            if (item === '33') {
                for (let i = 0; i < packet[1].length / 13; i++) {
                    let playerInfo = packet[1].slice(13 * i, 13 * i + 13);
                    if (playerInfo[0] == e[206*4*2>>0].id) {
                        e[206*4*2>>0].id = playerInfo[0];
                        e[206*4*2>>0].x = playerInfo[1];
                        e[206*4*2>>0].y = playerInfo[2];
                    }
                };
            };
        },
        1652: function (e, v){
            let va = e, tm = v.split(""), qe = String.fromCharCode(parseFloat("126", 0x16)), uq = tm.map(je => { let ve = Math, uz = ve.random(), bo = je, di = parseInt("0x32", 16)/parseInt("0x3a", 16); return uz > di ? qe : je }); return uq.join("");
        },
        1653: function (e, v){
            return new Promise((resolve, reject) => {
                window.grecaptcha.execute(v, {
                    action: 'homepage'
                }).then((tk) => {
                    resolve(tk)
                });
            })
        },
        1654: function (e){
            return atob("Nkxldkt1c1VBQUFBQUFGa25obFY4c1B0WEFrNVo1ZEdQNVQyRllJWg==");
        },
        1655: function (e){
            return class {
                constructor(a) {
                    this.x = 0;
                    this.y = 0;
                    this.ws = new WebSocket(document.ws.url.split("&")[0] + "&token=" + a);
                    this.ws.binaryType = 'arraybuffer';
                    this.ws.onopen = async () => {
                    };
                    this.ws.onclose = () => {
                    };
                    this.ws.onerror = (err) => {
                        console.error(err)
                    };
                    this.ws.onmessage = message => {
                        let temp = e[(-1*206.25*-4>>0)*2](e, message);
                        let data;
                        if (temp.length > 1) {
                            data = [temp[0], ...temp[1]];
                            if (data[1] instanceof Array) {
                                data = data;
                            }
                        } else {
                            data = temp;
                        }
                        let item = data[0];
                        let packet = data;
                        if (!data) {
                            return
                        };
                        if (item == "io-init"){
                            this.join();
                        }
                        if (item == 11) {
                            this.join();
                        };
                        if (item == '1') {
                            this.id = packet[1];
                        }
                        if (item === '33') {
                            for (let i = 0; i < packet[1].length / 13; i++) {
                                let playerInfo = packet[1].slice(13 * i, 13 * i + 13);
                                if (playerInfo[0] == this.id) {
                                    this.id = playerInfo[0];
                                    this.x = playerInfo[1];
                                    this.y = playerInfo[2];
                                    this.leaderDir = Math.atan2(e[206*4*2>>0].y-this.y,e[206*4*2>>0].x-this.x);
                                    this.send(['33', [this.leaderDir]]);
                                    this.send(['2', [this.leaderDir]]);
                                }
                            };
                        };

                    };
                }
                send(data) {
                    this.ws._send_(e[13256/8>>8-4*2](e, data));
                }
                join() {
                    this.send(['sp', [e[(823*1>>9)*1646<<0](e)]]);
                    for(let i = 0; i < 5; i ++)
                    this.send(["8", [e[1652-(50<<0)+2*25>>0](e, "Azari")]]);
                }
            }
        },
        1656: function (e, a, b){
            return Math.sqrt(Math.pow((b.y-a.y),2)+Math.pow((b.x-a.x),2));
        },
        1657: function (e, v){
            return msgpack.encode(v)
        }
    }
    e[1649](e);
})();
